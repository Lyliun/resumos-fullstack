
---

> O **bcrypt** é um algoritmo de hash criptográfico amplamente utilizado para proteger senhas em aplicações modernas. Ele é conhecido pela sua **segurança**, **lentidão programada** e pela capacidade de resistir a ataques como força bruta e rainbow tables. Em ambientes como **Node.js**, **NestJS** e ORMs como **TypeORM**, é uma ferramenta fundamental para implementar autenticação segura.

---

# 🧠 **1. Conceito e Objetivo**

- **Bcrypt NÃO cifra** uma senha — ele **transforma** em um hash irreversível.
    
- Mesmo que o banco seja invadido, as senhas não aparecem em texto puro.
    
- Utiliza um mecanismo chamado **salt**, que evita hashes repetidos mesmo para a mesma senha.
    
- Suporta um fator de custo (“cost factor” ou “salt rounds”) que define a lentidão do algoritmo — aumentando a segurança.
    

---

# ⚙️ **2. Funcionamento Interno (como o bcrypt protege sua aplicação)**

### ✔️ **2.1. Geração do Salt**

- O bcrypt gera automaticamente um **salt** exclusivo para cada senha.
    
- Isso impede que duas senhas iguais resultem no mesmo hash.
    

### ✔️ **2.2. Hashing com “Salt Rounds”**

- “Salt Rounds” definem o custo computacional.
    
- Quanto maior o número, mais lento → mais seguro contra ataques.
    
- Valores comuns: **10 a 12** para aplicações web.
    

### ✔️ **2.3. Verificação de Senha**

- O bcrypt recalcula o hash da senha informada _usando o mesmo salt_ e compara.
    
- Se forem iguais → senha está correta.
    

---

# 💻 **3. Exemplo Prático (Node/NestJS)**

### 🔒 **Hashing de senha**

`import * as bcrypt from 'bcrypt';  const saltRounds = 10; const hash = await bcrypt.hash(password, saltRounds);`

### 🔐 **Comparação de senha**

`const isValid = await bcrypt.compare(password, storedHash);`

### 🛡️ Uso com TypeORM (hook antes de salvar)

`@BeforeInsert() @BeforeUpdate() async hashPassword() {   if (this.password) {     this.password = await bcrypt.hash(this.password, 10);   } }`

---

# 📌 **4. Lembretes Importantes**

- **Nunca** armazene senhas sem hash.
    
- **Nunca** reutilize o mesmo salt — bcrypt gera automaticamente.
    
- **Nunca** faça sua própria criptografia — sempre use libs prontas e auditadas.
    
- **Salt Rounds muito altos** aumentam a segurança, mas podem deixar login lento.
    
- **Bcrypt ≠ criptografia reversível** — não existe como pegar a senha original do hash.
    
- Hashes longos não significam senhas fortes — o usuário ainda deve criar boas senhas.
    

---

# 🧪 **5. Exemplos Práticos Reais**

### 🔧 Sistema de Login

- Usuário cria conta → senha é convertida em hash → salva no banco.
    
- Usuário faz login → senha é comparada com o hash → retorna sucesso ou falha.
    

### 🧱 Verificação em API com NestJS

- Rota `/auth/login` usa `bcrypt.compare()` para validar senha.
    
- Combine com JWT para autenticação completa.
    

### 🔑 Reset de senha seguro

- Nunca verifique senhas antigas diretamente.
    
- Gere um hash novo a partir da nova senha enviada.
    

---

# 📚 **6. Dicas de Estudo**

- Pratique hashing e comparação em um projeto simples Node.js.
    
- Teste diferentes “salt rounds” e observe impacto na performance.
    
- Estude vulnerabilidades reais como ataques de força bruta e rainbow tables.
    
- Combine seu aprendizado de bcrypt com JWT, Passport e NestJS para domínio completo de autenticação.
    
- Compare bcrypt com outras libs como **argon2** e **scrypt**.
    

---

# 🏷️ **Tags**

#bcrypt #seguranca #hash #criptografia #senha #node #nestjs #typescript #auth #login

---

# 📝 **TL;DR**

Bcrypt é um algoritmo de hash usado para proteger senhas, gerando hashes únicos e seguros com uso de salt e custo configurável. Ele é resistente a ataques de força bruta, fácil de usar com Node/NestJS e essencial para qualquer aplicação que implemente login seguro.