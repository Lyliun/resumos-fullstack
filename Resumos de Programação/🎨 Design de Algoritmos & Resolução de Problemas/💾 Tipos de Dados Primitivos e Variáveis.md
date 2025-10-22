
> Os **tipos de dados** definem **que tipo de informação** uma variável pode armazenar.  
> Já as **variáveis** são “caixinhas de memória” usadas para **guardar valores** que o algoritmo manipula.  
> 	Entender bem esses dois conceitos é essencial pra **qualquer linguagem de programação**.

## 🧩 O que são Variáveis?

Uma **variável** é um **espaço na memória do computador** que armazena um valor que pode mudar durante a execução do programa.

💡 **Pense assim:**  
É como uma **etiqueta em uma gaveta** onde guardamos um valor.  
Podemos abrir, trocar ou consultar o que está dentro.

📘 **Exemplo em Portugol:**

`Var    nome: caractere    idade: inteiro    altura: real  Início    leia(nome)    leia(idade)    leia(altura)    escreva("Olá ", nome, "! Você tem ", idade, " anos e ", altura, "m de altura.") Fim`

---

## 🧠 Regras Gerais para Variáveis

✅ Devem ter **nomes descritivos e sem espaços**  
✅ **Não podem começar com números**  
✅ **Não usar acentos ou caracteres especiais**  
✅ O nome da variável deve representar **o que ela guarda**

📘 **Exemplos válidos:** `nota`, `mediaFinal`, `idadeAluno`  
❌ **Inválidos:** `1nota`, `média-final`, `idade aluno`

---

## 💡 O que são Tipos de Dados?

Os **tipos de dados primitivos** indicam **que tipo de informação** será armazenada na variável (números, textos, lógicos etc).  
Cada tipo ocupa um espaço diferente na memória e tem funções específicas.

---

## 📘 Tipos de Dados Primitivos

|Tipo|Descrição|Exemplo de Valor|Uso Comum|
|---|---|---|---|
|**inteiro**|Números inteiros (sem parte decimal)|`10`, `-5`, `0`|Contagens, idades, quantidades|
|**real**|Números decimais|`3.14`, `-0.5`|Médias, alturas, preços|
|**caractere**|Um único símbolo|`'A'`, `'b'`, `'9'`|Letras isoladas|
|**literal**|Cadeia de caracteres (texto)|`"Lia"`, `"Olá mundo"`|Nomes, mensagens|
|**lógico**|Verdadeiro ou falso|`verdadeiro`, `falso`|Condições e decisões|

---

### 🧮 Exemplo em Portugol:

`Var    idade: inteiro    altura: real    nome: literal    aprovado: logico  Início    idade <- 19    altura <- 1.68    nome <- "Lia"    aprovado <- verdadeiro     escreva(nome, " tem ", idade, " anos, ", altura, "m de altura. Aprovado? ", aprovado) Fim`

📘 **Saída esperada:**  
`Lia tem 19 anos, 1.68m de altura. Aprovado? verdadeiro`

---

## 🧩 Conversão entre Tipos de Dados

> Em algumas situações, é necessário **converter** um tipo de dado em outro (ex: número → texto).

|Conversão|Descrição|Exemplo|
|---|---|---|
|**inteiro → real**|Adiciona casas decimais|`3 → 3.0`|
|**real → inteiro**|Remove as casas decimais|`3.9 → 3`|
|**literal → inteiro**|Converte texto numérico|`"10" → 10`|
|**inteiro → literal**|Transforma número em texto|`10 → "10"`|

📘 Em Portugol, geralmente usamos funções como `inteiro()`, `real()`, ou `literal()` para conversões.

---

## 🔍 Operações com Variáveis

Exemplo prático de cálculo com variáveis:

`Var    nota1, nota2, media: real  Início    leia(nota1)    leia(nota2)    media <- (nota1 + nota2) / 2    escreva("A média é: ", media) Fim`

---

## 🧾 Lembretes Importantes

🧠 **1. Declara antes de usar:**  
Sempre **declare as variáveis no início do algoritmo**, dentro da seção `Var`.

⚙️ **2. Tipos devem ser compatíveis:**  
Não dá pra somar um `literal` (texto) com um `inteiro` (número) sem conversão.

🧮 **3. Valores podem mudar:**  
Variáveis podem ter **novos valores atribuídos** ao longo do algoritmo.

`contador <- 0 contador <- contador + 1`

💬 **4. Diferença entre variável e constante:**  
Uma **constante** tem valor **fixo** e **não pode ser alterada**.

`Const    PI = 3.14`

---

## 💬 Dicas de Estudo

✅ **Treina a declaração e o uso de variáveis** no Visualg ou Portugol Studio  
✅ Cria **algoritmos simples** (como cálculo de média, IMC ou troco) pra fixar o conceito  
✅ Faz **exercícios de conversão de tipos** pra entender compatibilidade  
✅ Revisa sempre o **tipo correto** pra cada informação (ex: idade → inteiro, nome → literal)

---

## 🧾 TL;DR

> 🧠 **Variáveis** são espaços na memória usados para armazenar dados.  
> 💾 **Tipos primitivos** determinam o formato e o tipo de dado armazenado.  
> ⚙️ Juntos, eles formam a base para **todo o processamento lógico e matemático** nos algoritmos.

---

## 🏷️ Tags

#variáveis #tiposdedados #algoritmos #portugol #lógica #generation #estudos