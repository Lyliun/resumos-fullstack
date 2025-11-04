Conjunto de regras e práticas que definem como as _branches_ devem ser criadas e mescladas (_merged_) para organizar o desenvolvimento, isolar novas funcionalidades e garantir a estabilidade do código em produção.

### 📘 Propósito

Um fluxo de versionamento define a estratégia de _branching_ para:

- **Isolamento:** Trabalhar em funcionalidades sem afetar o código principal.
    
- **Colaboração:** Gerenciar contribuições de múltiplos desenvolvedores.
    
- **Estabilidade:** Garantir que a _branch_ de produção (`main`) esteja sempre funcionando.
    

### ⚙️ As Branches Principais

Neste modelo, o desenvolvimento é organizado em torno de **branches de longo prazo** e **branches de suporte/curto prazo**.

|Branch|Tipo|Propósito|
|---|---|---|
|**`main`**|De Longo Prazo|Contém o código que está **em produção**. Deve ser sempre estável e _deployable_.|
|**`develop`**|De Longo Prazo|Contém o código mais recente, com todas as _features_ prontas para o próximo lançamento (ambiente de QA/Staging).|
|**`feature/`**|De Curto Prazo|Usada para desenvolver uma **nova funcionalidade**. Criada a partir de `develop` e mesclada de volta em `develop`.|
|**`hotfix/`**|De Curto Prazo|Usada para aplicar **correções urgentes** diretamente no código de produção (`main`).|

Export to Sheets

### 🔄 O Ciclo de Desenvolvimento (Feature Branch Workflow)

O fluxo padrão para a criação de uma nova funcionalidade (feature) segue estes passos:

1. **Preparação:** A _branch_ `develop` é criada a partir da `main`.
    
2. **Criação da Feature:** O desenvolvedor cria uma _branch de funcionalidade_ a partir da **`develop`**.
    
    - `git checkout -b feature/nome-da-feature develop`
        
3. **Desenvolvimento:** O desenvolvedor trabalha e faz _commits_ **apenas** na sua `feature/`.
    
    - `git add .`
        
    - `git commit -m "feat: login de usuário concluído"`
        
4. **Integração (PR):** Ao finalizar, ele envia a _branch_ para o repositório remoto (`git push`) e abre um **Pull Request (PR)**, solicitando que a sua _feature_ seja mesclada em `develop`.
    
5. **Merge:** Após revisão e aprovação (code review), a _feature branch_ é mesclada na **`develop`**.
    
6. **Lançamento (Release):** Quando a `develop` acumula _features_ suficientes e está estável, ela é mesclada na **`main`** para o lançamento de uma nova versão de produção.
    

### 💬 Comandos Chave no Fluxo

|Comando|Uso no Fluxo|Onde Usar|
|---|---|---|
|`git checkout -b`|Criar a branch de trabalho.|`git checkout -b feature/minha-feature develop`|
|`git push`|Enviar a branch local para o repositório remoto.|`git push origin feature/minha-feature`|
|`git pull origin develop`|Puxar o código mais recente da `develop` para manter a `feature` atualizada.|Dentro da sua branch `feature/`|
|`git switch develop`|Trocar para a branch `develop`.|Antes ou depois de um merge.|
|`git merge feature/x`|Unir o código da _feature_ na `develop`.|Dentro da branch `develop`|

Export to Sheets

### 🧠 Dicas e Lembretes

- 🔸 **NUNCA** commite ou faça push diretamente na `main` ou `develop` (exceto em casos muito específicos ou _hotfixes_).
    
- 🔸 Use prefixos claros nos nomes das branches: `feature/`, `bugfix/`, `hotfix/`.
    
- 🔸 **Fast-Forward Merge:** Se a branch `develop` não avançou enquanto você trabalhava, o merge pode ser rápido.
    
- 🔸 **No Fast-Forward Merge:** O mais comum em fluxos organizados. O `merge` cria um **novo commit** na `develop` que aponta para o merge dos históricos. _É o preferido para manter o histórico claro._
    
- 🔸 O **GitHub Flow** é uma versão simplificada: usa apenas `main` e _feature branches_.
    

### 🚀 TL;DR

O Git Flow organiza o desenvolvimento em _branches_ especializadas (`main` para produção e `develop` para integração) para garantir que as novas funcionalidades (`feature/`) sejam criadas e testadas isoladamente antes de serem integradas.

### 🏷️ Tags

#git #gitflow #versionamento #branch #colaboracao #generation #fundamentos