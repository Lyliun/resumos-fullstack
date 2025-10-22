
> As **estruturas de controle** definem **como o fluxo de execução** de um algoritmo acontece.  
	São fundamentais em **lógica de programação**, pois permitem controlar **a ordem, as decisões e repetições** das instruções.

## 🧩 Tipos de Estruturas de Controle

1. **Estrutura Sequencial** → executa comandos em ordem.
    
2. **Estrutura Condicional (Decisão)** → executa comandos conforme condições.
    
3. **Estrutura de Repetição (Laços)** → repete comandos enquanto uma condição for verdadeira.

## ⚙️ 1. Estrutura Sequencial

> É o tipo mais simples: as instruções são executadas **na ordem em que aparecem**.  
> Cada comando é executado **uma única vez**, de cima para baixo.

### 📘 Exemplo em pseudocódigo:

`Início     Ler A, B     Soma ← A + B     Escrever "Resultado:", Soma Fim`

### 💻 Exemplo em Python:

`a = int(input("Digite o primeiro número: ")) b = int(input("Digite o segundo número: ")) soma = a + b print("Resultado:", soma)`

💡 **Resumo:**  
Não há desvios ou repetições — apenas **execução linear**.

---

## 🔀 2. Estruturas Condicionais (Decisão)

> Permitem que o programa **escolha** qual caminho seguir com base em uma **condição lógica (verdadeira ou falsa)**.  
> Usadas para **tomar decisões** dentro do código.

### 📘 Tipos de Condicionais

|Tipo|Estrutura|Descrição|Exemplo|
|---|---|---|---|
|**Simples**|`if`|Executa um bloco **somente se** a condição for verdadeira.|Se idade ≥ 18 → “Pode votar”|
|**Composta**|`if / else`|Executa um bloco se a condição for **verdadeira**, e outro se for **falsa**.|Se média ≥ 7 → “Aprovado” senão “Reprovado”|
|**Encadeada**|`if / elif / else`|Verifica várias condições diferentes.|Se nota ≥ 9 → “Excelente” senão se nota ≥ 7 → “Aprovado” senão “Reprovado”|

### 💻 Exemplo em Python:

`nota = float(input("Digite sua nota: "))  if nota >= 9:     print("Excelente!") elif nota >= 7:     print("Aprovado!") else:     print("Reprovado!")`

💡 **Resumo:**  
As estruturas condicionais tornam o algoritmo **inteligente**, permitindo **escolhas e bifurcações** no fluxo do programa.

---

## 🔁 3. Estruturas de Repetição (Laços)

> Usadas quando é necessário **repetir instruções várias vezes**.  
> A repetição ocorre **enquanto** uma condição for **verdadeira** ou **até** que ela deixe de ser.

### 📘 Tipos de Laços

|Tipo|Palavra-chave|Descrição|Exemplo|
|---|---|---|---|
|**Enquanto (While)**|`while`|Repete **enquanto** a condição for verdadeira.|Enquanto contador < 10 → repetir|
|**Para (For)**|`for`|Executa um bloco um **número fixo de vezes**.|Para i de 1 até 5 → repetir|
|**Faça...Enquanto**|`do...while`|Executa **pelo menos uma vez**, e só depois verifica a condição.|(usado em outras linguagens como C ou Java)|

---

### 💻 Exemplo com `while` (Python)

`contador = 1 while contador <= 5:     print("Contagem:", contador)     contador += 1`

### 💻 Exemplo com `for` (Python)

`for i in range(1, 6):     print("Contagem:", i)`

💡 **Resumo:**  
As estruturas de repetição evitam código duplicado e são essenciais para tarefas **iterativas** (como percorrer listas, processar dados, etc.).

---

## 🧩 Comparativo Geral

|Tipo|Controle|Uso Típico|Palavra-chave (Python)|
|---|---|---|---|
|**Sequencial**|Ordem linear|Execução direta|—|
|**Condicional**|Escolha de caminhos|Tomar decisões|`if`, `elif`, `else`|
|**Repetição**|Repetir instruções|Laços, contadores|`for`, `while`|

---

## 💬 Boas Práticas

- ✨ **Indentação:** ajuda na legibilidade e estrutura do código.
    
- 🧠 **Evite laços infinitos:** sempre garanta que a condição de repetição possa ser encerrada.
    
- 🧩 **Use nomes claros:** para variáveis e condições.
    
- 🧪 **Teste com diferentes cenários:** para garantir que todos os caminhos funcionem.
    

---

## 🧾 TL;DR

> As **estruturas de controle** determinam **como e quando** as instruções de um programa são executadas:
> 
> - **Sequencial:** executa em ordem.
>     
> - **Condicional:** toma decisões.
>     
> - **Repetição:** repete ações até uma condição ser satisfeita.
>     

---

## 🏷️ Tags

#lógica #algoritmos #programação #estruturasdecontrole #generation #estudos
