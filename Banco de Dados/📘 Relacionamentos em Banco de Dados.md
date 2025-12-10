
---

> Os **relacionamentos** definem como as tabelas se conectam e trocam informações dentro de um banco de dados relacional. São essenciais para manter **coerência, organização, integridade dos dados e escalabilidade** na aplicação.

---
## **1. 🔗 O que são Relacionamentos?**

Relacionamentos representam **ligações lógicas** entre tabelas diferentes, permitindo que o banco de dados modele estruturas complexas do mundo real.

Eles funcionam por meio de:

- **Chave Primária (PK)** → Identifica de forma única cada registro.
    
- **Chave Estrangeira (FK)** → Aponta para a PK de outra tabela, formando o elo de ligação.
    

---

## **2. 🧩 Tipos de Relacionamentos**

### **2.1 — Relacionamento 1:1 (Um para Um)**

Um registro A está ligado a **um único** registro B.

**Exemplo:**  
Tabela _usuário_ ↔ tabela _perfil_ (cada usuário tem 1 perfil).

**Quando usar:**

- Para separar dados sensíveis ou opcionais.
    
- Para otimizar leitura dividindo colunas pouco acessadas.
    

---

### **2.2 — Relacionamento 1:N (Um para Muitos)**

Um registro A pode estar ligado a **vários** registros B.  
É o tipo mais comum.

**Exemplo:**  
_Categorias_ → _Produtos_  
Uma categoria possui muitos produtos, mas cada produto tem **apenas uma** categoria.

**Implementação:**  
Coloca-se a **FK** na tabela do lado “muitos”.

---

### **2.3 — Relacionamento N:N (Muitos para Muitos)**

Vários registros A se relacionam com vários registros B.

**Exemplo:**  
_Cursos_ ↔ _Alunos_  
Um aluno pode fazer vários cursos, e um curso pode ter vários alunos.

**Como implementar no MySQL:**  
Criar uma **tabela intermediária**, também chamada de **tabela de junção** ou **join table**, contendo duas FKs:

`tb_alunos_cursos - id_aluno (FK) - id_curso (FK)`

---

## **3. 🏛 Integridade Referencial**

Conjunto de regras que garantem que os relacionamentos se mantenham consistentes.

### **3.1 — Restrições importantes**

- **FOREIGN KEY**
    
- **ON DELETE** (CASCADE, SET NULL, RESTRICT)
    
- **ON UPDATE** (idem)
    

### **3.2 — Por que é importante?**

Evita:

- Registros órfãos
    
- Erros de consistência
    
- Perda de dados acidental
    

**Exemplo prático:**  
Se deletar uma categoria, o que acontece com os produtos?

- `CASCADE`: todos os produtos ligados são apagados.
    
- `SET NULL`: a FK vira null.
    
- `RESTRICT`: impede a exclusão.
    

---

## **4. 🔍 Cardinalidade dos Relacionamentos**

Define quantos registros podem estar ligados de cada lado.

Principais tipos:

- **0 ou 1**
    
- **0 ou N**
    
- **1 ou N**
    
- **1 e somente 1**
    

Ajuda na modelagem do DER e na lógica da aplicação.

---

## **5. 🧪 Exemplo Prático (MySQL)**

### **Relacionamento 1:N**

`CREATE TABLE categorias (    id INT AUTO_INCREMENT PRIMARY KEY,    nome VARCHAR(100) NOT NULL );  CREATE TABLE produtos (    id INT AUTO_INCREMENT PRIMARY KEY,    nome VARCHAR(100) NOT NULL,    preco DECIMAL(10,2),    categoria_id INT,    FOREIGN KEY (categoria_id)       REFERENCES categorias(id)       ON DELETE SET NULL       ON UPDATE CASCADE );`

---

## **6. 🧠 Boas Práticas de Modelagem de Relacionamentos**

✔ Nomear FKs como `<tabela>_id`  
✔ Usar `CASCADE` apenas quando necessário  
✔ Criar índices nas FKs para melhorar consultas  
✔ Documentar relacionamentos no DER  
✔ Evitar relacionamentos desnecessários que aumentam acoplamento

---

## **7. 🎯 Por que Relacionamentos Importam no Desenvolvimento?**

Eles tornam o sistema:

- Mais coeso e organizado
    
- Mais eficiente em consultas
    
- Mais seguro
    
- Mais fácil de manter e escalar
    
- Alinhado com padrões profissionais de backend (NestJS, ORM, MVC)
    

No desenvolvimento com **TypeORM ou Prisma**, relacionamentos são recursos essenciais para:

- montar rotas
    
- criar serviços
    
- montar joins inteligentes
    
- reduzir queries manuais