
> As **estruturas condicionais** permitem que o programa **tome decisões** com base em certas condições.  
> 	São fundamentais para controlar o **fluxo lógico** de um algoritmo ou código.

## 🧩 Conceito

Uma **estrutura condicional** analisa uma **condição lógica (verdadeira ou falsa)** e executa diferentes blocos de código dependendo do resultado.  
Isso torna o programa **inteligente e dinâmico**, reagindo a diferentes situações.

💡 É como dizer ao computador:

> “Se isso acontecer, faça isso. Caso contrário, faça aquilo.”

---

## 🔀 Tipos de Estruturas Condicionais

### 🧠 **1. Condicional Simples**

Executa um bloco **somente se** a condição for **verdadeira**.

`se (idade >= 18) então     escreva("Pode dirigir") fimse`

🧩 Em JavaScript:

`if (idade >= 18) {   console.log("Pode dirigir"); }`

---

### ⚖️ **2. Condicional Composta**

Executa um bloco **se a condição for verdadeira**, e outro **se for falsa**.

`se (idade >= 18) então     escreva("Pode dirigir") senão     escreva("Ainda não pode dirigir") fimse`

🧩 Em JavaScript:

`if (idade >= 18) {   console.log("Pode dirigir"); } else {   console.log("Ainda não pode dirigir"); }`

---

### 🔁 **3. Condicional Encadeada**

Usada quando há **várias possibilidades**.

`se (nota >= 7) então     escreva("Aprovado") senão se (nota >= 5) então     escreva("Recuperação") senão     escreva("Reprovado") fimse`

🧩 Em JavaScript:

`if (nota >= 7) {   console.log("Aprovado"); } else if (nota >= 5) {   console.log("Recuperação"); } else {   console.log("Reprovado"); }`

---

### 🧭 **4. Estrutura de Escolha (switch/caso)**

Usada quando várias condições são comparadas com o **mesmo valor**.

`escolha (opcao)     caso 1:         escreva("Cadastrar usuário")     caso 2:         escreva("Listar usuários")     caso 3:         escreva("Sair")     outrocaso:         escreva("Opção inválida") fimescolha`

🧩 Em JavaScript:

`switch (opcao) {   case 1:     console.log("Cadastrar usuário");     break;   case 2:     console.log("Listar usuários");     break;   case 3:     console.log("Sair");     break;   default:     console.log("Opção inválida"); }`

---

## 💬 Lembretes

⚙️ **1. Condições sempre retornam verdadeiro (`true`) ou falso (`false`)**  
Exemplo: `idade >= 18` → retorna `true` ou `false`.

🔍 **2. Operadores lógicos e relacionais** são essenciais nas condições:

- `==`, `!=`, `>`, `<`, `>=`, `<=`
    
- `&&` (E), `||` (OU), `!` (NÃO)
    

🚨 **3. Sempre fechar as estruturas corretamente** (`fimse`, `}` ou `break` no caso do switch).

🧠 **4. Prefira switch** quando houver muitas comparações com o mesmo valor.

---

## 💡 Exemplos Práticos

`let temperatura = 30;  if (temperatura > 35) {   console.log("Muito quente!"); } else if (temperatura >= 25) {   console.log("Clima agradável."); } else {   console.log("Friozinho bom!"); }`

🔹 **Saída:** `Clima agradável.`

---

## 💬 Dicas de Estudo

✅ **1. Pratica com situações do cotidiano**, como idade, notas, login ou desconto.  
✅ **2. Faz fluxogramas antes de programar**, ajuda a visualizar o raciocínio lógico.  
✅ **3. Tenta reescrever condicionais com operadores lógicos combinados (`&&`, `||`).**  
✅ **4. Treina no Portugol Studio ou em um playground JavaScript (como o repl.it).**  
✅ **5. Refatora teus códigos antigos**: vê se há formas de simplificar condicionais.

---

## 🧾 TL;DR

> As **estruturas condicionais** definem **decisões** dentro de um programa.  
> São a base da **lógica de controle**, permitindo respostas diferentes conforme o contexto.  
> Dominar essas estruturas é o primeiro passo pra pensar como um programador. 💡

---

## 🏷️ Tags

#programação #lógica #condicional #portugol #javascript #fundamentos #generation