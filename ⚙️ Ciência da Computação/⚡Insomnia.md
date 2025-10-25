# ⚡ Insomnia — Testes de API REST

> Ferramenta gráfica para testar, documentar e automatizar requisições HTTP.  
> Muito usada no desenvolvimento e depuração de **APIs RESTful**.

---

## 🧠 O que é o Insomnia

O **Insomnia** é um **API Client** (cliente de API), semelhante ao Postman, que permite:

- Criar **requisições HTTP** (GET, POST, PUT, DELETE, PATCH, etc).
    
- Enviar e testar **corpos JSON**.
    
- Gerenciar **variáveis de ambiente** (como URLs e tokens).
    
- Salvar e organizar **coleções de requisições**.
    
- Ver respostas com **status code**, **tempo de resposta** e **corpo retornado**.
    

💡 Ideal para testar endpoints de **backends Node.js (Express)**, **Spring Boot**, **Django**, **Laravel**, entre outros.

---

## ⚙️ Estrutura do Insomnia

| Elemento                | Função                                                                 |
| ----------------------- | ---------------------------------------------------------------------- |
| **Workspace**           | Espaço de trabalho (pode ser pessoal ou de time).                      |
| **Request**             | Uma requisição HTTP específica (ex.: `GET /users`).                    |
| **Environment**         | Conjunto de variáveis configuráveis (ex.: `{{base_url}}`).             |
| **Collection / Folder** | Agrupamento de requisições relacionadas (ex.: Rotas de Usuário).       |
| **Body**                | Onde se define o conteúdo enviado (JSON, form, etc).                   |
| **Header**              | Define metadados da requisição (ex.: `Content-Type`, `Authorization`). |

---

## 🚀 Criando uma Requisição

1. Clique em **New Request** → Dê um nome → Escolha o método (`GET`, `POST`, etc).
    
2. No campo **URL**, insira o endpoint, por exemplo:
    
    `http://localhost:3000/api/users`
    
3. Configure:
    
    - **Headers**:
        
        `{ "Content-Type": "application/json" }`
        
    - **Body (POST/PUT)**:
        
        `{   "nome": "Lia Santos",   "email": "lia@generation.com" }`
        
4. Clique em **Send** para enviar a requisição.
    
5. Verifique a resposta na área de **Response** (status, tempo, JSON retornado, etc).
    

---

## 🌍 Métodos HTTP Principais

|Método|Função|Exemplo|
|---|---|---|
|**GET**|Buscar informações|`/usuarios`|
|**POST**|Criar novo registro|`/usuarios`|
|**PUT**|Atualizar registro inteiro|`/usuarios/1`|
|**PATCH**|Atualizar parcialmente|`/usuarios/1`|
|**DELETE**|Excluir registro|`/usuarios/1`|

---

## 🔐 Testando Rotas Autenticadas

1. Vá até a aba **Headers** e adicione:
    
    `Authorization: Bearer <seu_token_aqui>`
    
2. Se tiver variável de ambiente configurada:
    
    `Authorization: Bearer {{token}}`
    

💡 Isso é essencial pra testar APIs protegidas com JWT (JSON Web Token).

---

## 🧩 Variáveis de Ambiente

Tu pode criar variáveis pra não precisar reescrever URLs e tokens toda hora:

`{   "base_url": "http://localhost:3000/api",   "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6..." }`

E usar assim nas requisições:

`{{base_url}}/usuarios`

👉 As variáveis podem ser locais (workspace) ou globais (todos os projetos).

---

## 📂 Organização e Boas Práticas

- Cria uma **collection** pra cada projeto (ex.: “API Generation”).
    
- Divide em pastas como:
    
    - `/usuarios`
        
    - `/cursos`
        
    - `/matriculas`
        
- Nomeia as requisições claramente:
    
    - `GET — Listar Usuários`
        
    - `POST — Criar Usuário`
        
    - `DELETE — Excluir Usuário`
        
- Usa **descrições** pra anotar o que cada endpoint faz.
    
- Versiona o arquivo `.json` exportado no teu GitHub (backup).
    

---

## 🧠 Lembretes e Dicas

- ⚙️ Usa `Ctrl + Enter` pra enviar rapidamente a requisição.
    
- 🪶 Dá pra exportar e importar coleções (`Export Workspace`).
    
- 💬 Verifica sempre o **status code** da resposta:
    
    - `200 OK` → Sucesso
        
    - `201 Created` → Registro criado
        
    - `400 Bad Request` → Erro no corpo da requisição
        
    - `401 Unauthorized` → Falta de autenticação
        
    - `404 Not Found` → Rota inexistente
        
    - `500 Internal Server Error` → Erro no servidor
        
- 🧾 Usa **Plugins do Insomnia** pra gerar tokens JWT, timestamps, etc.
    
- 💡 Pode integrar com o **Git Sync** (versões recentes) pra salvar tudo no repositório.
    

---

## 🚀 TL;DR

> O **Insomnia** é uma ferramenta para enviar, testar e organizar requisições HTTP,  
> sendo essencial para desenvolver, depurar e documentar APIs REST.

---

## 🏷️ Tags

#insomnia #api #http #backend #generation #fullstack #ferramentas