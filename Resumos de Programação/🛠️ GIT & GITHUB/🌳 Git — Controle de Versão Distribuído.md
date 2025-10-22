Sistema fundamental para rastrear mudanças no código, permitir a colaboração em equipe e reverter estados anteriores de um projeto.

### 📘 O que é o Git

O Git é um **Sistema de Controle de Versão Distribuído (DVCS)** criado por Linus Torvalds.

Ele permite que cada desenvolvedor tenha uma cópia completa do histórico do projeto em sua máquina (distribuído), garantindo segurança e a possibilidade de trabalhar offline.

### ⚙️ Estrutura e Fluxo de Trabalho

O Git trabalha com três áreas principais no seu ambiente de desenvolvimento:

|Área|Descrição|Comandos Chave|
|---|---|---|
|**Working Directory** (Diretório de Trabalho)|Os arquivos que você está editando no momento.|`git status`|
|**Staging Area** (Área de Preparação)|Onde você _seleciona_ as mudanças que farão parte do próximo _commit_.|`git add`|
|**Local Repository** (Repositório Local)|O banco de dados onde os _commits_ são armazenados permanentemente na sua máquina.|`git commit`|


### 🧭 Comandos Essenciais (CLI)

Comandos básicos para iniciar e gerenciar um projeto localmente:

|Comando|Função|Exemplo|
|---|---|---|
|`git init`|Cria um novo repositório Git no diretório atual.|`git init`|
|`git clone`|Baixa um repositório remoto para a sua máquina.|`git clone [URL]`|
|`git add`|Adiciona alterações do Working Directory para a Staging Area.|`git add index.html` ou `git add .`|
|`git commit`|Salva as mudanças da Staging Area no Repositório Local.|`git commit -m "Nova feature de login"`|
|`git status`|Verifica quais arquivos foram modificados e em qual área estão.|`git status`|
|`git log`|Mostra o histórico de _commits_.|`git log --oneline`|
|`git diff`|Mostra as diferenças entre o Working Directory e a Staging Area (ou entre _commits_).|`git diff`|
|`git restore`|Desfaz alterações (dependendo da flag, pode ser na Staging ou no Working Directory).|`git restore arquivo.txt`|


### 💬 Branching e Colaboração

Recursos cruciais para trabalhar em equipes e desenvolver funcionalidades isoladamente:

|Comando|Função|Observação|
|---|---|---|
|`git branch`|Lista todas as _branches_ ou cria uma nova.|`git branch dev-nova-feature`|
|`git switch`|Troca para uma _branch_ existente.|`git switch main`|
|`git checkout -b`|Cria uma nova _branch_ e já troca para ela.|`git checkout -b nome-da-branch`|
|`git merge`|Junta o histórico de uma _branch_ em outra (ex.: _feature_ para _main_).|`git merge nome-da-branch`|
|`git push`|Envia seus _commits_ locais para o Repositório Remoto (ex.: GitHub).|`git push origin main`|
|`git pull`|Baixa o código mais recente do Remoto para o Local.|`git pull origin main`|


### 🧠 Boas Práticas e Lembretes

- **Commits Atômicos:** Faça _commits_ pequenos, focados em uma única mudança ou correção.
    
- **Mensagens Claras:** Escreva mensagens no _commit_ que expliquem _o quê_ e _por que_ a mudança foi feita.
    
- **`.gitignore`:** Use este arquivo para garantir que arquivos de configuração, dependências (`node_modules`) ou logs não sejam versionados.
    
- **`main` ou `master`:** Mantenha a _branch_ principal (geralmente `main`) sempre pronta para produção.
    
- **`git remote -v`:** Verifica a URL do repositório remoto (ex.: GitHub).

### 🚀 TL;DR

**Git** é o sistema de controle de versão que rastreia, gerencia e armazena todas as mudanças no código do projeto, permitindo colaboração e reversão de estados.
### 🏷️ Tags

#git #controledeversao #cli #github #branching #generation #fundamentos