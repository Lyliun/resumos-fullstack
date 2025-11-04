
> O **terminal (prompt de comando)** é uma ferramenta poderosa para **navegar, executar programas e automatizar tarefas**.  
> Aprender a usá-lo é essencial pra quem desenvolve software, administra sistemas ou trabalha com Git, Node.js e bancos de dados.

## 🧩 Conceito

O **terminal** é uma **interface de linha de comando (CLI)**.  
Em vez de usar janelas e botões, você **digita comandos** para interagir diretamente com o sistema operacional.

💡 É como conversar com o computador de forma direta e precisa.

---

## ⚙️ Terminais Mais Comuns

|Sistema|Terminal|Comando para abrir|
|---|---|---|
|**Windows**|Prompt de Comando (`cmd`) ou PowerShell|`Win + R` → `cmd`|
|**Linux**|Terminal padrão do sistema|`Ctrl + Alt + T`|
|**macOS**|Terminal (nativo)|Spotlight `⌘ + Espaço` → "Terminal"|

---

## 📁 Comandos de Navegação e Manipulação de Arquivos

|Ação|Windows (`cmd`)|Linux/macOS|Descrição|
|---|---|---|---|
|Ver diretório atual|`cd`|`pwd`|Mostra o caminho da pasta atual|
|Listar arquivos|`dir`|`ls`|Lista arquivos e pastas|
|Entrar em pasta|`cd nome_pasta`|`cd nome_pasta`|Muda o diretório atual|
|Voltar uma pasta|`cd..`|`cd ..`|Volta um nível|
|Limpar tela|`cls`|`clear`|Limpa o terminal|
|Criar pasta|`mkdir nome`|`mkdir nome`|Cria um novo diretório|
|Apagar pasta|`rmdir nome`|`rmdir nome` ou `rm -r nome`|Remove uma pasta|
|Apagar arquivo|`del nome.txt`|`rm nome.txt`|Exclui um arquivo|
|Abrir pasta atual|`start .`|`open .` (mac) / `xdg-open .` (Linux)|Abre no gerenciador de arquivos|

💡 **Exemplo prático:**

`# Criar um projeto e entrar nele mkdir projeto-js cd projeto-js`

---

## 🔍 Comandos de Sistema

|Ação|Windows|Linux/macOS|Descrição|
|---|---|---|---|
|Exibir data|`date /t`|`date`|Mostra a data atual|
|Exibir hora|`time /t`|`date "+%H:%M"`|Mostra a hora atual|
|Exibir IP da máquina|`ipconfig`|`ifconfig` ou `ip a`|Mostra informações de rede|
|Ver processos ativos|`tasklist`|`ps` ou `top`|Lista processos em execução|
|Encerrar processo|`taskkill /PID 1234`|`kill 1234`|Encerra um processo|
|Ver espaço em disco|`wmic logicaldisk get size,freespace,caption`|`df -h`|Mostra o uso de disco|
|Informações do sistema|`systeminfo`|`uname -a`|Exibe detalhes do sistema operacional|

💡 **Exemplo prático:**

`# Ver informações sobre o sistema e IP systeminfo ipconfig`

---

## 🧮 Comandos Úteis para Desenvolvedores

|Ação|Comando|Descrição|
|---|---|---|
|Ver versão do Node.js|`node -v`|Mostra a versão instalada|
|Ver versão do npm|`npm -v`|Mostra a versão do gerenciador de pacotes|
|Verificar instalação do Git|`git --version`|Mostra se o Git está instalado|
|Iniciar repositório Git|`git init`|Cria um novo repositório local|
|Rodar servidor local (Node)|`npm start`|Inicia um projeto Node.js|
|Instalar pacote|`npm install nome_pacote`|Adiciona dependência ao projeto|

💡 **Exemplo prático:**

`# Iniciar um projeto Node e subir um servidor npm init -y npm install express npm start`

---

## 📦 Comandos de Rede e Teste de Conexão

|Ação|Windows|Linux/macOS|Descrição|
|---|---|---|---|
|Testar conexão com site|`ping google.com`|`ping google.com`|Verifica conectividade|
|Ver rota de rede|`tracert google.com`|`traceroute google.com`|Mostra o caminho dos pacotes|
|Exibir DNS|`nslookup google.com`|`dig google.com`|Mostra IPs e DNS de um domínio|
|Mostrar portas abertas|`netstat -an`|`netstat -tuln`|Lista conexões e portas abertas|

💡 **Exemplo prático:**

`ping github.com`

---

## 🧩 Comandos Específicos do PowerShell (Windows)

|Ação|Comando|Descrição|
|---|---|---|
|Listar diretório|`Get-ChildItem`|Igual a `dir`|
|Copiar arquivo|`Copy-Item origem destino`|Copia um arquivo|
|Mover arquivo|`Move-Item origem destino`|Move arquivo/pasta|
|Apagar arquivo|`Remove-Item nome.txt`|Exclui arquivo|
|Exibir processos|`Get-Process`|Mostra processos ativos|

---

## 💬 Lembretes Importantes

🧠 **1. Cuidado com comandos de exclusão:**  
`rm -rf` (Linux/mac) e `del` (Windows) **não pedem confirmação** — podem apagar tudo!

⚙️ **2. Maiúsculas/minúsculas importam no Linux e macOS**, mas não no Windows.  
📁 **3. Use `Tab` para autocompletar nomes de arquivos e pastas.**  
🔄 **4. Comandos podem ser combinados:**

`cd projetos && dir`

Executa o segundo comando só se o primeiro der certo.

---

## 💬 Dicas de Estudo

✅ Cria uma **nota no Obsidian com seções separadas por sistema** (Windows, Linux, Mac).  
✅ Pratica comandos de **navegação e criação de pastas** até se sentir confortável.  
✅ Usa o **Terminal integrado do VS Code** — é prático pra testar tudo no mesmo lugar.  
✅ Faz uma **tabela de atalhos pessoais** com os comandos que mais usa.  
✅ Testa sempre em **pastas de teste** antes de usar comandos de exclusão.

---

## 🧾 TL;DR

> O **terminal** é a base do controle sobre o sistema e o ambiente de desenvolvimento.  
> Dominar comandos básicos permite **navegar, criar, testar e automatizar** com agilidade.  
> Saber usá-lo bem é uma das **habilidades mais valiosas** pra quem programa. 💪

---

## 🏷️ Tags

#terminal #prompt #cmd #linux #mac #windows #comandos #desenvolvimento #estudos #generation