
> Os **operadores** são símbolos usados para **realizar operações matemáticas, comparações ou lógicas** dentro de um algoritmo.  
> 	Eles são fundamentais para o **processamento de dados**, permitindo que o programa calcule, compare e tome decisões.

## 🧩 Tipos de Operadores

Os operadores se dividem em quatro grandes grupos principais:

1. ➕ **Aritméticos** — realizam cálculos matemáticos
    
2. 📝 **De Atribuição** — armazenam valores em variáveis
    
3. ⚖️ **Relacionais** — comparam valores
    
4. 🔁 **Lógicos** — avaliam expressões verdadeiras ou falsas
    

---

## ➕ Operadores Aritméticos

Usados para realizar **operações matemáticas** básicas.

|Operador|Descrição|Exemplo|Resultado|
|---|---|---|---|
|`+`|Adição|`5 + 3`|`8`|
|`-`|Subtração|`10 - 4`|`6`|
|`*`|Multiplicação|`7 * 2`|`14`|
|`/`|Divisão|`8 / 2`|`4`|
|`%`|Resto da divisão (módulo)|`10 % 3`|`1`|
|`^`|Potenciação (em algumas linguagens)|`2 ^ 3`|`8`|

📘 **Lembrete:**

- Em algumas linguagens, potenciação é feita com `**` (ex: Python).
    
- A operação `%` é muito usada em **estruturas de repetição** para verificar se um número é par ou ímpar.
    

---

### 💡 Exemplo prático (em pseudocódigo)

`num1 <- 10 num2 <- 3 soma <- num1 + num2 resto <- num1 % num2 escreva("Soma: ", soma) escreva("Resto: ", resto)`

---

## 📝 Operadores de Atribuição

Usados para **armazenar ou atualizar valores** em variáveis.  
O símbolo `←` (ou `=` em linguagens de programação) representa a **atribuição de valor**.

|Operador|Descrição|Exemplo|Resultado|
|---|---|---|---|
|`←` ou `=`|Atribui valor|`x ← 5`|`x = 5`|
|`+=`|Soma e atribui|`x += 2`|`x = x + 2`|
|`-=`|Subtrai e atribui|`x -= 3`|`x = x - 3`|
|`*=`|Multiplica e atribui|`x *= 4`|`x = x * 4`|
|`/=`|Divide e atribui|`x /= 2`|`x = x / 2`|

📘 **Lembrete:**  
Esses operadores servem para **atualizar variáveis** de forma mais rápida e legível.

---

### 💡 Exemplo prático

`contador <- 0 contador <- contador + 1 // forma comum contador += 1             // forma reduzida (em linguagens reais)`

---

## ⚖️ Operadores Relacionais

Usados para **comparar valores** e gerar um **resultado lógico** (`verdadeiro` ou `falso`).  
Esses operadores são essenciais em **estruturas condicionais** (como `se`, `enquanto`, etc.).

|Operador|Descrição|Exemplo|Resultado|
|---|---|---|---|
|`=`|Igual a|`5 = 5`|verdadeiro|
|`<>`|Diferente de|`5 <> 3`|verdadeiro|
|`>`|Maior que|`7 > 4`|verdadeiro|
|`<`|Menor que|`2 < 5`|verdadeiro|
|`>=`|Maior ou igual|`4 >= 4`|verdadeiro|
|`<=`|Menor ou igual|`3 <= 8`|verdadeiro|

📘 **Lembrete:**

- Esses operadores **não atribuem valores**, apenas **comparam**.
    
- O resultado sempre será **lógico**: verdadeiro (`true`) ou falso (`false`).
    

---

### 💡 Exemplo prático

`idade <- 18  se (idade >= 18) então    escreva("Pode votar.") senao    escreva("Não pode votar.") fimse`

---

## 🔁 Operadores Lógicos

Usados para **combinar expressões booleanas (verdadeiras ou falsas)**.  
Permitem construir **condições mais complexas** em decisões e repetições.

|Operador|Significado|Exemplo|Resultado|
|---|---|---|---|
|`e`|Verdadeiro se **ambas** forem verdadeiras|`(x > 0) e (x < 10)`|verdadeiro se `x` estiver entre 1 e 9|
|`ou`|Verdadeiro se **pelo menos uma** for verdadeira|`(x = 0) ou (y = 0)`|verdadeiro se `x` ou `y` for 0|
|`não`|Inverte o valor lógico|`não(x > 5)`|verdadeiro se `x <= 5`|

📘 **Lembrete:**

- Em algumas linguagens, os operadores lógicos são escritos como `&&`, `||` e `!`.
    
- Muito usados em condições compostas dentro de `if`, `while` e `for`.
    

---

### 💡 Exemplo prático

`idade <- 25 tem_carteira <- verdadeiro  se (idade >= 18 e tem_carteira = verdadeiro) então    escreva("Pode dirigir.") senao    escreva("Não pode dirigir.") fimse`

---

## 🧾 Resumo Geral

|Categoria|Operadores|Função Principal|
|---|---|---|
|**Aritméticos**|`+`, `-`, `*`, `/`, `%`, `^`|Realizam cálculos|
|**Atribuição**|`=`, `+=`, `-=`, `*=`, `/=`|Atribuem valores|
|**Relacionais**|`=`, `<>`, `>`, `<`, `>=`, `<=`|Comparam valores|
|**Lógicos**|`e`, `ou`, `não`|Avaliam condições|

---

## 💬 Dicas de Estudo

✅ Memoriza a **diferença entre “= (atribuição)” e “== (comparação)”** — isso muda de linguagem pra linguagem.  
✅ Usa **operadores relacionais e lógicos juntos** pra testar condições complexas.  
✅ Testa combinações em **Portugol Studio ou Visualg** pra entender como as condições se comportam.  
✅ Sempre **fecha condições** com `fimse`, `fimenquanto`, etc. pra manter clareza.

---

## 🧾 TL;DR

> Os **operadores** são símbolos que permitem **calcular, comparar e controlar a lógica** dos programas.  
> Eles são fundamentais para expressar **regras, condições e cálculos** dentro dos algoritmos.

---

## 🏷️ Tags

#operadores #aritméticos #relacionais #lógicos #atribuição #portugol #lógica #generation #estudos