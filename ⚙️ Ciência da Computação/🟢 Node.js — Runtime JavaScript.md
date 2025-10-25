Ambiente de execução (runtime) que permite que o JavaScript seja executado fora do navegador, tipicamente no lado do servidor (backend).

### 📘 O que é o Node.js

O Node.js é um **ambiente de execução JavaScript** de código aberto, construído sobre o **V8 Engine** do Google Chrome.

Seu design é **não-bloqueante (non-blocking)** e orientado a eventos (**event-driven**), o que o torna extremamente eficiente para lidar com muitas conexões simultâneas (ideal para APIs e servidores web).

### ⚙️ Conceitos Chave

|Conceito|Descrição|
|---|---|
|**V8 Engine**|O motor C++ que o Google Chrome usa para compilar JS em código de máquina. É o coração do Node.js.|
|**Event Loop**|O mecanismo que permite ao Node.js lidar com operações assíncronas (ex.: IO de arquivo, requisições HTTP) de forma não-bloqueante, mantendo a performance.|
|**Non-Blocking I/O**|O Node.js não espera que uma operação de entrada/saída (I/O) termine. Ele inicia a operação, segue processando outras tarefas e retorna o resultado via _callback_ ou _Promise_.|
|**Módulos**|São blocos de código encapsulados. Podem ser **Core** (nativos do Node, como `fs`, `http`) ou **Externos** (baixados via npm, como `express`).|


### 📦 npm — Gerenciador de Pacotes

O **npm (Node Package Manager)** é o maior registro de bibliotecas de código aberto do mundo e a principal ferramenta para gerenciar as dependências de um projeto Node.

|Comando|Função|Exemplo|
|---|---|---|
|`npm init`|Cria o arquivo `package.json`, que registra as informações do projeto e suas dependências.|`npm init -y` (cria com padrões)|
|`npm install`|Baixa as dependências listadas no `package.json` para a pasta `node_modules`.|`npm install`|
|`npm install [pacote]`|Instala um pacote específico no projeto.|`npm install express`|
|`npm install [pacote] -g`|Instala um pacote globalmente (para uso via CLI).|`npm install nodemon -g`|
|`npm install [pacote] --save-dev`|Instala o pacote apenas para desenvolvimento (ex.: testes, linters).|`npm install jest --save-dev`|
|`npm start`|Executa o script definido como `start` no `package.json`.|`npm start`|


### 🖥️ Comandos Essenciais (CLI)

- `node [arquivo.js]`: Executa um arquivo JavaScript diretamente com o Node.
    
    - Exemplo: `node server.js`
        
- `npm run [script]`: Executa um script personalizado definido no `package.json`.
    
    - Exemplo: `npm run dev` (se `dev` estiver definido)
        

### 🚀 Uso Prático

O Node.js é ideal para construir:

1. **APIs RESTful:** Usando _frameworks_ como o Express.js ou NestJS.
    
2. **Servidores Web:** Lidar com requisições HTTP e roteamento.
    
3. **Aplicações em Tempo Real:** Chats, jogos (devido ao seu modelo assíncrono).
    
4. **Ferramentas CLI:** Automatizar tarefas via linha de comando.
    

### 🧠 Lembretes e Dicas

- **`package-lock.json`:** Garante que todos da equipe usem exatamente as mesmas versões de dependência.
    
- **Assincronicidade:** Sempre use `Promises` (`async/await`) ou _callbacks_ ao lidar com I/O (banco de dados, arquivos, HTTP) para não bloquear o Event Loop.
    
- **`nodemon`:** Uma ferramenta útil para desenvolvimento que reinicia automaticamente o servidor Node sempre que você salva uma alteração no código.

### 🚀 TL;DR

**Node.js** é o ambiente de execução não-bloqueante que permite rodar JavaScript no lado do servidor (backend), ideal para construir APIs rápidas e escaláveis.

### 🏷️ Tags

#nodejs #javascript #backend #npm #eventloop #fullstack #generation