
> As **estruturas de repetição** (ou **laços de repetição**) permitem executar um **conjunto de instruções várias vezes**, economizando código e evitando repetições manuais.

## 🧩 Conceito

Uma **estrutura de repetição** cria um **ciclo controlado**, onde um bloco de código é **executado enquanto uma condição for verdadeira**.

💡 Em vez de copiar e colar o mesmo comando várias vezes, o programa repete automaticamente até que a condição seja **falsa**.

> “Repita isso até que algo mude.”

---

## 🔄 Tipos de Estruturas de Repetição

### 🧠 **1. Estrutura “Enquanto” (While)**

Repete **enquanto** a condição for **verdadeira**.  
Se for **falsa desde o início**, o bloco **não é executado**.

`enquanto (contador <= 5) faça     escreva(contador)     contador <- contador + 1 fimenquanto`

🧩 Em JavaScript:

`let contador = 1;  while (contador <= 5) {   console.log(contador);   contador++; }`

🔹 **Saída:** 1 2 3 4 5

💡 Ideal quando **não se sabe exatamente quantas vezes** o laço será executado.

---

### 🧮 **2. Estrutura “Repita...Até” (Do While)**

Executa o bloco **pelo menos uma vez**, depois **testa a condição**.

`repita     escreva(contador)     contador <- contador + 1 até (contador > 5)`

🧩 Em JavaScript:

`let contador = 1;  do {   console.log(contador);   contador++; } while (contador <= 5);`

🔹 **Saída:** 1 2 3 4 5

💡 Útil quando **o bloco precisa ser executado pelo menos uma vez**, mesmo que a condição comece falsa.

---

### 🔢 **3. Estrutura “Para” (For)**

Usada quando **se sabe exatamente quantas vezes repetir**.

`para contador de 1 até 5 faça     escreva(contador) fimpara`

🧩 Em JavaScript:

`for (let contador = 1; contador <= 5; contador++) {   console.log(contador); }`

🔹 **Saída:** 1 2 3 4 5

💡 Muito usada em **listas, vetores, arrays e loops controlados**.

---

## 💬 Lembretes

⚙️ **1. Sempre inicialize e atualize variáveis de controle**  
→ Evita **loops infinitos**.  
Exemplo:

`while (x < 10) {   // precisa aumentar x dentro do laço!   x++; }`

🔁 **2. Loops infinitos** só devem ser usados quando há **condição de parada interna**, como `break`.

🚨 **3. Use `break` e `continue` com cuidado**:

- `break` → **interrompe** o loop.
    
- `continue` → **pula** para a próxima iteração.
    

💡 **4. “for” é mais comum para contagens; “while” para condições variáveis.**

---

## 💡 Exemplos Práticos

### 💬 Exemplo 1: Soma de números

`let soma = 0;  for (let i = 1; i <= 5; i++) {   soma += i; } console.log("Soma total:", soma);`

🔹 **Saída:** `Soma total: 15`

---

### 💬 Exemplo 2: Verificação de senha (com do...while)

`let senha = ""; do {   senha = prompt("Digite a senha:"); } while (senha !== "1234");  console.log("Acesso permitido!");`

💡 O bloco é executado pelo menos uma vez, mesmo que a senha esteja errada.

---

### 💬 Exemplo 3: Loop com condição interna

`for (let i = 1; i <= 10; i++) {   if (i === 5) break;   console.log(i); }`

🔹 **Saída:** `1 2 3 4`

🧠 O `break` encerra o loop quando `i` é 5.

---

## 💬 Dicas de Estudo

✅ **1. Pratica laços em situações simples:** contagens, somas e listas.  
✅ **2. Faz comparações entre “for”, “while” e “do...while” pra entender quando usar cada um.**  
✅ **3. Cria fluxogramas com setas mostrando o “voltar” da repetição.**  
✅ **4. Testa loops que dependem de entradas do usuário.**  
✅ **5. Simula loops infinitos de forma controlada pra entender o comportamento.**

---

## 🧾 TL;DR

> As **estruturas de repetição** automatizam execuções repetitivas, tornando o código mais limpo e eficiente.  
> O segredo está em **controlar a condição** — saber **quando começar, quando parar e quando repetir**.  
> Dominar loops é um passo essencial pra criar programas dinâmicos e inteligentes. 🔁

---

## 🏷️ Tags

#programação #lógica #repetição #loop #portugol #javascript #fundamentos #generation