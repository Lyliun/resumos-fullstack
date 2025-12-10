
---

## **1️⃣ O que é um Banco de Dados?**

> Um **banco de dados** é um sistema organizado para armazenar, gerenciar e recuperar informações de forma eficiente.  
> Ele é utilizado para guardar dados estruturados (ex.: usuários, produtos, pedidos) garantindo **integridade**, **segurança** e **consistência**.

---

## **2️⃣ Dados, Informações e Conhecimento**

- **Dado:** elemento bruto, sem contexto.  
    _Ex.: “23”, “Maria”, “Azul”._
    
- **Informação:** dado com significado.  
    _Ex.: “Maria tem 23 anos”._
    
- **Conhecimento:** informação aplicada para tomada de decisão.  
    _Ex.: “Como a Maria é jovem, pode estar no público-alvo do produto X”._
    

👉 Bancos de dados transformam dados → em informação → que apoia o conhecimento.

---

## **3️⃣ Sistema de Gerenciamento de Banco de Dados (SGBD)**

Software responsável pelo controle dos dados.  
No seu caso: **MySQL**.

Funções principais:

- Criar e organizar tabelas
    
- Controlar acessos
    
- Garantir integridade
    
- Otimizar consultas
    
- Realizar backups e restaurações
    

---

## **4️⃣ Modelos de Banco de Dados**

### **🔹 Relacional (mais usado — MySQL)**

- Dados organizados em tabelas
    
- Linhas = registros
    
- Colunas = atributos
    
- Uso de chaves e relações
    

### **🔹 NoSQL (MongoDB, Redis, Cassandra)**

- Focado em flexibilidade
    
- Formatos: documentos, chave-valor, grafos
    
- Usado em apps que lidam com grandes volumes não estruturados
    

---

## **5️⃣ Tabelas e Esquemas**

### **🧱 Tabela**

Estrutura principal para armazenar dados.  
Exemplo: `tb_usuarios`, `tb_produtos`.

### **📐 Esquema (Schema)**

Organização lógica das tabelas do banco.  
Pense como uma “pasta” que agrupa tudo.

---

## **6️⃣ Chaves**

### **🔑 Chave Primária (PK)**

Identifica unicamente um registro.

- Não pode repetir
    
- Não pode ser nula  
    Ex.: `id INT AUTO_INCREMENT PRIMARY KEY`
    

### **🔗 Chave Estrangeira (FK)**

Relaciona tabelas.

- Garante integridade referencial
    
- Liga tabelas “pai” e “filha”  
    Ex.: `id_categoria` em `tb_produtos`
    

---

## **7️⃣ Tipos de Dados (MySQL)**

Alguns dos mais comuns:

### **Numéricos**

- `INT`
    
- `DECIMAL`
    
- `BIGINT`
    

### **Texto**

- `VARCHAR(n)`
    
- `TEXT`
    

### **Datas**

- `DATE`
    
- `DATETIME`
    
- `TIMESTAMP`
    

### **Booleanos**

- `BOOLEAN` (0 ou 1)
    

---

## **8️⃣ Operações Fundamentais (CRUD)**

CRUCIAL para qualquer banco.

|Operação|SQL|Significado|
|---|---|---|
|**Create**|INSERT|Criar registro|
|**Read**|SELECT|Ler dados|
|**Update**|UPDATE|Atualizar dados|
|**Delete**|DELETE|Apagar dados|

Essas operações sustentam qualquer aplicação — API, sistema web, app mobile etc.

---

## **9️⃣ Normalização**

Processo de organizar o banco para evitar:

❌ duplicação de dados  
❌ inconsistências  
❌ lentidão

Benefícios:  
✔ bancos limpos  
✔ economia de espaço  
✔ maior integridade

Exemplos de formas normais (NF):

- 1NF → dados atômicos
    
- 2NF → separar dados que dependem de outras colunas
    
- 3NF → eliminar dependências transitivas
    

---

## **🔟 Integridade dos Dados**

Regras que mantêm o banco confiável.

- **Integridade de domínio** → tipo correto
    
- **Integridade de entidade** → PK válida
    
- **Integridade referencial** → FK válida
    
- **Integridade de negócio** → regras específicas da aplicação (ex.: idade mínima 18)
    

---

## **1️⃣1️⃣ Transações**

Um conjunto de operações que devem ser executadas juntas.  
SGBDs seguem o padrão **ACID**:

- **A**tomicidade
    
- **C**onsistência
    
- **I**solamento
    
- **D**urabilidade
    

Exemplo: pagamento + atualização de estoque.

---

## **1️⃣2️⃣ Índices**

Estruturas que aceleram consultas.  
Como se fosse um índice de livro.

Prós:  
✔ velocidade  
Contras:  
❌ ocupam espaço  
❌ tornam INSERT/UPDATE mais pesados

---

## **1️⃣3️⃣ Views (Visões)**

Consultas salvas que funcionam como “tabelas virtuais”.  
Ótimas para:

- Segurança
    
- Simplificar queries complexas
    
- Controle de acesso
    

---

## **1️⃣4️⃣ Stored Procedures e Functions**

Código SQL armazenado no banco.

✔ desempenho melhor  
✔ padronização  
✔ mais segurança

---

## **1️⃣5️⃣ Joins — A Base das Relações**

Conectam dados de várias tabelas.

- **INNER JOIN**
    
- **LEFT JOIN**
    
- **RIGHT JOIN**
    
- **FULL JOIN** (não no MySQL nativamente)
    

Exemplo: Produtos + Categorias.

---

# **📌 Conclusão Geral**

Os **conceitos fundamentais** em MySQL são a base para qualquer aplicação profissional.  
Entender tabelas, chaves, normalização, transações e relacionamentos é o que permite criar sistemas **seguro, limpos, rápidos e escaláveis**.

