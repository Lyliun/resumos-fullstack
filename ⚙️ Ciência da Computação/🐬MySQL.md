# 🐬 MySQL — Banco de Dados Relacional

> Sistema de gerenciamento de banco de dados relacional (SGBD) amplamente usado em aplicações web, open source e compatível com o padrão SQL.

---

## 📘 O que é o MySQL

O **MySQL** é um **SGBD (Sistema Gerenciador de Banco de Dados)** que utiliza o modelo **relacional** — ou seja, organiza dados em **tabelas** interligadas por **chaves**.  
Ele usa a linguagem **SQL (Structured Query Language)** para manipular e consultar dados.

📍 Desenvolvido originalmente pela **MySQL AB**, hoje pertence à **Oracle Corporation**.

---

## ⚙️ Estrutura e Conceitos Fundamentais

|Conceito|Descrição|
|---|---|
|**Banco de Dados**|Conjunto de tabelas que armazenam informações relacionadas.|
|**Tabela**|Estrutura organizada em linhas (registros) e colunas (campos).|
|**Campo / Coluna**|Define o tipo de dado armazenado (nome, idade, e-mail, etc).|
|**Registro / Linha**|Cada entrada de dados (exemplo: um usuário).|
|**Chave Primária (PRIMARY KEY)**|Identifica de forma única cada registro na tabela.|
|**Chave Estrangeira (FOREIGN KEY)**|Cria relação entre tabelas diferentes.|
|**Índices (INDEX)**|Aceleram buscas e consultas.|
|**View**|“Tabelas virtuais” baseadas em consultas SQL.|
|**Stored Procedures / Functions**|Blocos de código SQL salvos no banco para reutilização.|

---

## 🧱 Tipos de Dados Comuns

| Tipo                            | Exemplo              | Uso                                  |
| ------------------------------- | -------------------- | ------------------------------------ |
| `INT`, `BIGINT`                 | 1, 42, 9999          | Números inteiros                     |
| `DECIMAL`, `FLOAT`              | 10.5, 99.99          | Valores numéricos com casas decimais |
| `CHAR`, `VARCHAR`               | "Lia", "Generation"  | Texto                                |
| `TEXT`, `LONGTEXT`              | Texto longo          | Artigos, descrições                  |
| `DATE`, `DATETIME`, `TIMESTAMP` | 2025-10-14, 10:30:00 | Datas e horários                     |
| `BOOLEAN`                       | TRUE/FALSE           | Lógico (verdadeiro/falso)            |

---

## 💬 Comandos SQL Essenciais

### 🔹 Criação e Estrutura

`CREATE DATABASE generation; USE generation;  CREATE TABLE alunos (   id INT AUTO_INCREMENT PRIMARY KEY,   nome VARCHAR(100),   idade INT,   email VARCHAR(100) );`

### 🔹 Inserção de Dados

`INSERT INTO alunos (nome, idade, email) VALUES ('Lia Santos', 24, 'lia@email.com');`

### 🔹 Consulta de Dados

`SELECT * FROM alunos; SELECT nome, idade FROM alunos WHERE idade > 18;`

### 🔹 Atualização e Remoção

`UPDATE alunos SET email = 'novo@email.com' WHERE id = 1; DELETE FROM alunos WHERE id = 1;`

### 🔹 Relacionamento entre Tabelas

`CREATE TABLE cursos (   id INT AUTO_INCREMENT PRIMARY KEY,   nome VARCHAR(100) );  CREATE TABLE matriculas (   id INT AUTO_INCREMENT PRIMARY KEY,   aluno_id INT,   curso_id INT,   FOREIGN KEY (aluno_id) REFERENCES alunos(id),   FOREIGN KEY (curso_id) REFERENCES cursos(id) );`

---

## 🔄 Relacionamentos Entre Tabelas

| Tipo                         | Descrição                                    | Exemplo                                |
| ---------------------------- | -------------------------------------------- | -------------------------------------- |
| **1:1 (um para um)**         | Um registro se relaciona com apenas um outro | Usuário → Perfil                       |
| **1:N (um para muitos)**     | Um registro se relaciona com vários          | Curso → Alunos                         |
| **N:N (muitos para muitos)** | Vários registros se relacionam entre si      | Alunos ↔ Cursos (tabela intermediária) |

---

## 🧠 Boas Práticas e Lembretes

- 🔸 Sempre use **PRIMARY KEY** em cada tabela.
    
- 🔸 Prefira **nomes em minúsculas e no plural** (`alunos`, `cursos`).
    
- 🔸 Evite **redundância**: use chaves estrangeiras em vez de repetir informações.
    
- 🔸 **BACKUP!** Faça cópias regulares do banco (`mysqldump`).
    
- 🔸 Use **índices** em colunas frequentemente consultadas.
    
- 🔸 Mantenha as queries **otimizadas** (evite `SELECT *` quando possível).
    
- 🔸 Utilize **transações (`BEGIN`, `COMMIT`, `ROLLBACK`)** para garantir integridade.
    

---

## 💡 Dicas Avançadas

- O MySQL usa **storage engines**, sendo o **InnoDB** o padrão (com suporte a transações e integridade referencial).
    
- Dá pra acessar via **MySQL Workbench**, **CLI** ou ferramentas como **phpMyAdmin**.
    
- Pode ser integrado em apps com **Node.js**, **Java**, **Python**, **PHP**, etc.
    
- Suporta **views**, **triggers**, **procedures** e **eventos agendados**.


## 🖥️ Comandos Úteis no Terminal (CLI)

> Comandos básicos e intermediários para trabalhar com o MySQL pelo **PowerShell**, **Git Bash** ou **terminal integrado** do VS Code.

---

### 🔹 Acessar o MySQL

`mysql -u root -p`

- `-u root` → usuário (padrão: root)
    
- `-p` → pede senha após pressionar Enter
    

📍 Se quiser entrar sem senha (apenas em ambiente local):

`mysql -u root`

---

### 🔹 Comandos Gerais

|Comando|Função|
|---|---|
|`SHOW DATABASES;`|Lista todos os bancos de dados disponíveis|
|`CREATE DATABASE nome_do_banco;`|Cria um novo banco de dados|
|`DROP DATABASE nome_do_banco;`|Exclui um banco de dados|
|`USE nome_do_banco;`|Seleciona o banco de dados a ser usado|
|`SHOW TABLES;`|Mostra todas as tabelas dentro do banco atual|
|`DESCRIBE nome_tabela;`|Mostra estrutura (colunas, tipos, chaves) da tabela|

---

### 🔹 Gerenciar Tabelas

`CREATE TABLE usuarios (   id INT AUTO_INCREMENT PRIMARY KEY,   nome VARCHAR(100),   email VARCHAR(100),   criado_em TIMESTAMP DEFAULT CURRENT_TIMESTAMP );`

Outros comandos:

|Comando|Função|
|---|---|
|`ALTER TABLE nome_tabela ADD coluna VARCHAR(50);`|Adiciona uma nova coluna|
|`ALTER TABLE nome_tabela DROP COLUMN coluna;`|Remove uma coluna|
|`DROP TABLE nome_tabela;`|Deleta uma tabela inteira|

---

### 🔹 Inserir, Consultar e Atualizar

`INSERT INTO usuarios (nome, email) VALUES ('Lia Santos', 'lia@email.com'); SELECT * FROM usuarios; UPDATE usuarios SET nome = 'Lia Generation' WHERE id = 1; DELETE FROM usuarios WHERE id = 1;`

---

### 🔹 Sair do MySQL

`exit;`

ou

`\q`

---

### 🔹 Backup e Restauração

`# Exportar banco de dados (backup) mysqldump -u root -p nome_do_banco > backup.sql  # Importar (restaurar) banco de dados mysql -u root -p nome_do_banco < backup.sql`

💡 Dica: guarda o arquivo `backup.sql` no GitHub (privado) ou em nuvem, pra não perder tuas tabelas quando estiver praticando.

---

### 🔹 Dicas Rápidas

- 🔸 Sempre finaliza cada comando com **ponto e vírgula ( ; )**.
    
- 🔸 Usa `\c` pra cancelar um comando inacabado.
    
- 🔸 Usa `\! clear` pra limpar a tela dentro do MySQL.
    
- 🔸 O comando `status;` mostra informações da sessão atual.
    
- 🔸 Tu pode usar `SOURCE caminho_do_arquivo.sql;` pra executar scripts salvos.
    

---

## 🧠 Resumo Final

> Saber usar o terminal é essencial pra administrar e testar bancos de dados MySQL.  
> Os comandos de **criação, inserção e consulta** são a base — e dominar o **backup/restauração** garante segurança e controle do teu progresso.

---

## 🚀 TL;DR

> MySQL é um banco de dados relacional que usa SQL para gerenciar informações em tabelas interligadas.  
> É rápido, gratuito, seguro e amplamente utilizado em sistemas web modernos.

---

## 🏷️ Tags

#mysql #bancodedados #sql #fullstack #generation #backend #client #sql #bancodedados #backend #fullstack