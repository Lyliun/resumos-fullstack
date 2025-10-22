
> Um **algoritmo** pode ser representado de várias formas, dependendo do contexto e da clareza desejada.  
> As três mais comuns são:  
> 	**Descrição Narrativa**, **Fluxograma** e **Pseudocódigo (ou Portugol)**.
> 		Essas representações ajudam a **planejar e visualizar a lógica** antes de escrever o código em uma linguagem de programação real.

## 🗣️ 1. Descrição Narrativa

> É a forma **mais simples e textual** de descrever um algoritmo.  
> Usa a **linguagem natural (português)** para explicar **passo a passo** o que deve ser feito.

### 💡 Características:

- Escrita em **forma de texto corrido**
    
- **Fácil de entender**, mesmo sem conhecimento técnico
    
- Ideal para **planejamento inicial ou documentação**
    

### 🧾 Exemplo:

> **Algoritmo para somar dois números:**
> 
> 1. Ler dois números.
>     
> 2. Somar esses números.
>     
> 3. Exibir o resultado da soma.
>     

### ✅ Vantagens:

- Simples e intuitiva.
    
- Boa para explicar a lógica a pessoas não técnicas.
    

### ⚠️ Desvantagens:

- Pode se tornar **ambígua** (interpretações diferentes).
    
- Difícil de converter diretamente em código.
    

---

## 🔄 2. Fluxograma

> É uma **representação gráfica** do algoritmo.  
> Usa **símbolos padronizados** para mostrar **o fluxo de execução** das instruções.

### 💡 Características:

- Usa **formas geométricas** e **setas**.
    
- Facilita a **visualização do caminho lógico** do algoritmo.
    
- Ideal para **analisar a estrutura** e identificar **erros lógicos**.
    

---

### 🧩 Principais Símbolos:

| Símbolo             | Nome          | Função                               |
| ------------------- | ------------- | ------------------------------------ |
| ⏺️ **Elipse/Oval**  | Início/Fim    | Indica o começo e o fim do algoritmo |
| ⬛ **Retângulo**     | Processamento | Representa uma operação ou cálculo   |
| ⬜ **Paralelogramo** | Entrada/Saída | Ler ou mostrar informações           |
| 🔺 **Losangulo**    | Decisão       | Representa uma condição (Sim/Não)    |
| ➡️ **Seta**         | Conector      | Indica o fluxo de execução           |

---

### 🧾 Exemplo: _Algoritmo para verificar se o número é positivo_

`⏺️ Início ⬜ Ler número 🔺 número > 0 ?    ↳ Sim → ⬜ Escrever "Positivo"    ↳ Não → ⬜ Escrever "Negativo ou zero" ⏺️ Fim`

💡 **Resumo:**  
O fluxograma é ótimo para **visualizar e depurar** a lógica antes da implementação.

---

## 💻 3. Pseudocódigo / Portugol

> O **pseudocódigo** (ou **Portugol**) é uma **linguagem intermediária**, usada para **escrever algoritmos de forma estruturada**, próxima de uma linguagem de programação, mas ainda em português.

### 💡 Características:

- Linguagem **sem regras fixas**, mas com **estrutura lógica clara**.
    
- Usa **comandos comuns de programação** (leia, escreva, se, enquanto, para...).
    
- Muito utilizado no ensino de **lógica e algoritmos**.
    

---

### 🧾 Exemplo em Pseudocódigo:

`Algoritmo "Verificar número" Var    num: inteiro Início    escreva("Digite um número: ")    leia(num)     se (num > 0) então        escreva("O número é positivo.")    senao        escreva("O número é negativo ou zero.")    fimse Fim`

---

### ✅ Vantagens:

- **Fácil de converter em código real** (Python, C, Java etc.)
    
- Ajuda a **entender a lógica sem se preocupar com sintaxe real**.
    
- Facilita a **transição para linguagens de programação**.
    

### ⚠️ Desvantagens:

- Não é executável (não roda no computador diretamente).
    
- Cada pessoa ou instituição pode usar **variações diferentes** da sintaxe.
    

---

## 🧩 Comparativo Geral

|Tipo|Estilo|Vantagem|Ideal para|
|---|---|---|---|
|**Descrição Narrativa**|Texto simples|Fácil entendimento|Planejamento inicial|
|**Fluxograma**|Visual|Clareza no fluxo|Visualizar decisões e repetições|
|**Pseudocódigo / Portugol**|Estruturado|Próximo da programação real|Aprender lógica e escrever algoritmos|

---

## 💬 Dica Extra

> 🔁 Uma boa prática é **começar com a descrição narrativa**,  
> depois **desenhar o fluxograma**,  
> e finalmente **escrever o pseudocódigo**.  
> Assim, tu garante clareza **tanto lógica quanto visual** antes de programar. 💡

---

## 🧾 TL;DR

> Um **algoritmo** pode ser descrito de 3 formas:
> 
> - **Narrativa:** explicação textual simples.
>     
> - **Fluxograma:** diagrama visual do fluxo lógico.
>     
> - **Pseudocódigo/Portugol:** representação estruturada próxima da programação.
>     

---

## 🏷️ Tags

#algoritmos #fluxograma #pseudocódigo #portugol #lógica #generation #estudos