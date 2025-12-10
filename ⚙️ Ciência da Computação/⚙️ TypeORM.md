
---

## 🌐 **1. Conceito Geral**

> TypeORM é um **ORM (Object-Relational Mapping)** para **TypeScript** e **JavaScript**, utilizado principalmente com **Node.js**. Ele permite trabalhar com bancos de dados relacionais usando **classes e objetos** no lugar de SQL puro.  
> Seu objetivo é facilitar a modelagem de dados, abstrair queries complexas, garantir tipagem forte e tornar o código mais estruturado e escalável — especialmente em aplicações **NestJS**.

Funciona com:

- **MySQL**, **PostgreSQL**, **MariaDB**, **SQLite**, **SQL Server**, entre outros.

---

# 🧱 **2. Fundamentos Essenciais**

### **2.1 Entidades**

São classes que representam tabelas do banco.

`@Entity() export class Usuario {   @PrimaryGeneratedColumn()   id: number;    @Column()   nome: string; }`

---

### **2.2 Repositórios**

Objeto que permite executar operações de banco (CRUD).

`const usuarios = await usuarioRepository.find();`

---

### **2.3 DataSource (configuração)**

Arquivo com as informações de conexão.

`export const AppDataSource = new DataSource({   type: 'mysql',   host: 'localhost',   username: 'root',   password: '',   database: 'meubanco',   entities: [Usuario],   synchronize: true, });`

---

### **2.4 Migrations**

Permitem versionar alterações no banco de dados.

`npx typeorm migration:generate -n CriarTabelaUsuario npx typeorm migration:run`

---

### **2.5 Decorators importantes**

- `@Entity()`
    
- `@Column()`
    
- `@PrimaryGeneratedColumn()`
    
- `@CreateDateColumn()`
    
- `@UpdateDateColumn()`
    
- `@ManyToOne()`
    
- `@OneToMany()`
    
- `@ManyToMany()`
    
- `@JoinColumn()`
    

---

# 🔗 **3. Relacionamentos**

### **3.1 One-to-One**

`@OneToOne(() => Perfil) @JoinColumn() perfil: Perfil;`

### **3.2 One-to-Many / Many-to-One**

`@OneToMany(() => Postagem, post => post.usuario) postagens: Postagem[];  @ManyToOne(() => Usuario, usuario => usuario.postagens) usuario: Usuario;`

### **3.3 Many-to-Many**

`@ManyToMany(() => Tag) @JoinTable() tags: Tag[];`

---

# 📊 **4. Consultas no TypeORM**

### **4.1 find**

`repository.find(); repository.find({ where: { nome: "Lia" } });`

### **4.2 findOne**

`repository.findOne({ where: { id: 1 } });`

### **4.3 Query Builder**

Ferramenta poderosa para buscas complexas.

`const usuarios = await repository   .createQueryBuilder("usuario")   .leftJoinAndSelect("usuario.postagens", "post")   .where("usuario.ativo = :ativo", { ativo: true })   .getMany();`

---

# 🧩 **5. Lembretes Importantes**

- `synchronize: true` só para desenvolvimento (perigoso em produção).
    
- Sempre manter migrations atualizadas para evitar inconsistências.
    
- Utilize DTOs com NestJS para validar e organizar entradas de dados.
    
- TypeORM funciona melhor com **TypeScript**, aproveitando tipagem estática.
    
- Relacionamentos precisam ser bidirecionais quando houver carregamento de dados complexos.
    

---

# 🧪 **6. Exemplos Práticos**

### **Criar um registro**

`const usuario = repository.create({ nome: "Lia" }); await repository.save(usuario);`

### **Atualizar**

`await repository.update(id, { nome: "Lia Santos" });`

### **Deletar**

`await repository.delete(id);`

### **Buscar com relações**

`repository.find({ relations: ["postagens"] });`

---

# 🎓 **7. Dicas de Estudo**

- Pratique criando pequenas entidades e relacionando-as (ex.: Usuário → Postagens).
    
- Reescreva consultas com QueryBuilder e sem QueryBuilder para entender a diferença.
    
- Leia o log SQL no terminal (`logging: true`) e veja como o TypeORM traduz suas operações.
    
- Combine TypeORM com NestJS para consolidar padrões profissionais.
    
- Teste intencionalmente erros de relacionamento para aprender a resolver (`cascade`, `onDelete`).
    

---

# 📌 **TL;DR**

TypeORM é um ORM para TypeScript/Node que transforma tabelas em classes. Oferece abstrações para CRUD, relacionamentos, migrations e query builder. Facilita organização, tipagem e escalabilidade, sendo amplamente usado com NestJS.

---

# 🏷️ **Tags**

#typeorm #orm #node #typescript #nestjs #mysql #backend #database #estudos