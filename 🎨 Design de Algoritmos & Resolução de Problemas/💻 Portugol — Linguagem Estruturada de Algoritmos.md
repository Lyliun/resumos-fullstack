
> O **Portugol** é uma **linguagem de descrição de algoritmos** que se parece muito com uma linguagem de programação real,  
> mas é escrita em **português estruturado** e **não executável**.

É amplamente usada para **ensinar lógica de programação**, pois ajuda a entender **como o computador “pensa”** sem se preocupar com a sintaxe rígida de linguagens como C, Java ou Python.

## 🧠 Conceito

> 🔹 O Portugol é uma **linguagem algorítmica estruturada**, usada para **descrever a lógica de um programa**.  
> 🔹 É baseado em **estruturas de controle** (sequência, decisão e repetição).  
> 🔹 Seu objetivo principal é **facilitar o aprendizado de lógica** e **planejar algoritmos** antes da implementação.

---

## 🧩 Estrutura Básica de um Algoritmo em Portugol

Um algoritmo em Portugol normalmente segue **essa estrutura geral**:

`Algoritmo "Nome_do_Algoritmo"  Var    // Declaração de variáveis    nome: caractere    idade: inteiro    altura: real  Início    // Corpo principal do algoritmo    escreva("Digite seu nome: ")    leia(nome)     escreva("Digite sua idade: ")    leia(idade)     escreva("Olá, ", nome, "! Você tem ", idade, " anos.") Fim`

---

### 🔍 Explicação da Estrutura:

|Parte|Função|
|---|---|
|**Algoritmo "..."**|Define o nome do programa.|
|**Var**|Declaração das variáveis usadas.|
|**Início**|Marca o começo da execução do algoritmo.|
|**Fim**|Indica o fim do algoritmo.|
|**leia()**|Entrada de dados (usuário digita algo).|
|**escreva()**|Saída de dados (mostra algo na tela).|

---

## 🧮 Tipos de Dados

No Portugol, as variáveis devem ter um tipo definido.

|Tipo|Descrição|Exemplo|
|---|---|---|
|**inteiro**|Números inteiros|`10`, `-5`, `42`|
|**real**|Números decimais|`3.14`, `-0.5`, `2.75`|
|**caractere**|Um único símbolo|`'A'`, `'b'`|
|**literal**|Texto (cadeia de caracteres)|`"Lia"`, `"Generation"`|
|**logico**|Verdadeiro ou falso|`verdadeiro`, `falso`|

---

## 🔄 Estruturas de Controle

O Portugol trabalha com as três estruturas clássicas da programação:

---

### 🧱 **1. Estrutura Sequencial**

> As instruções são executadas **uma após a outra**, em ordem.

`escreva("Digite dois números: ") leia(a) leia(b)  soma <- a + b  escreva("Resultado: ", soma)`

---

### ⚖️ **2. Estrutura Condicional (Decisão)**

> Permite **escolher um caminho** com base em uma condição (verdadeira ou falsa).

#### 🔸 Simples:

`se (idade >= 18) então    escreva("Maior de idade.") fimse`

#### 🔸 Com “senão”:

`se (idade >= 18) então    escreva("Maior de idade.") senao    escreva("Menor de idade.") fimse`

---

### 🔁 **3. Estrutura de Repetição (Laços)**

> Executa **um conjunto de instruções várias vezes**, enquanto uma condição for verdadeira.

#### 🔹 Enquanto:

`contador <- 1 enquanto (contador <= 5) faça    escreva("Contagem: ", contador)    contador <- contador + 1 fimenquanto`

#### 🔹 Para:

`para i de 1 até 5 faça    escreva("Número: ", i) fimpara`

#### 🔹 Repita:

`repita    escreva("Digite um número positivo: ")    leia(num) ate (num > 0)`

---

## 🧩 Operadores Mais Usados

|Tipo|Operadores|Exemplo|
|---|---|---|
|**Aritméticos**|`+`, `-`, `*`, `/`, `%`|`soma <- a + b`|
|**Relacionais**|`=`, `<>`, `>`, `<`, `>=`, `<=`|`se (x <> 0)`|
|**Lógicos**|`e`, `ou`, `não`|`se (idade >= 18 e idade <= 60)`|

---

## 💬 Boas Práticas no Portugol

✅ Usar **nomes de variáveis descritivos** (`nota1`, `media`, `idadeAluno`)  
✅ Indentar o código para **deixar mais legível**  
✅ Comentar trechos importantes com `//`  
✅ Sempre testar as **estruturas condicionais e de repetição**

---

## 💻 Ferramentas Populares para Usar Portugol

|Ferramenta|Descrição|
|---|---|
|**Visualg**|Programa clássico e leve para testar algoritmos em Portugol|
|**Portugol Studio**|Ambiente moderno com interface intuitiva e execução visual dos algoritmos|
|**Pseudocode Online**|Alternativa online para testar lógica em pseudocódigo/Portugol|

---

## 📌 Resumo Rápido

|Conceito|Descrição|
|---|---|
|**Portugol**|Linguagem estruturada em português usada para descrever algoritmos|
|**Principal uso**|Ensino de lógica de programação|
|**Estruturas básicas**|Sequência, decisão e repetição|
|**Comandos principais**|`leia`, `escreva`, `se`, `para`, `enquanto`, `repita`|
|**Ferramenta recomendada**|Visualg ou Portugol Studio|

---

## 🧾 TL;DR

> O **Portugol** é uma linguagem em português usada para **ensinar lógica de programação**.  
> Ele permite criar algoritmos estruturados com comandos simples como `leia`, `escreva`, `se` e `enquanto`.  
> Apesar de não ser executável em computadores reais, é essencial para **entender a base da lógica** antes de aprender linguagens como **Python, Java ou JavaScript**.

---

## 🏷️ Tags

#portugol #algoritmos #visualg #lógica #generation #estudos