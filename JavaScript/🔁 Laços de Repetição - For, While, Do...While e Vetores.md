### 💡 Conceito

Os **laços de repetição** (ou _loops_) permitem que o programa **repita automaticamente um conjunto de instruções** enquanto uma condição for verdadeira.  
Eles são fundamentais pra evitar código repetitivo e automatizar tarefas.

### 🧠 Lembretes

- Um **loop** precisa de três partes principais:
    
    1. **Inicialização** → onde começa.
        
    2. **Condição** → até quando repete.
        
    3. **Incremento/Decremento** → como avança.
        
- Os principais tipos são:
    
    - `for` → quando sabemos quantas vezes repetir.
        
    - `while` → quando não sabemos quantas vezes, mas há uma condição.
        
    - `do...while` → executa pelo menos uma vez, mesmo se a condição for falsa.
        
- **Vetores (arrays)** armazenam **vários valores em uma única variável** — ideais pra usar junto com loops.
    

---

### 🧩 Exemplos Práticos

#### 🔸 For

``for (let i = 1; i <= 5; i++) {   console.log(`Número: ${i}`); }``

🟢 Executa de 1 a 5, repetindo a ação a cada incremento.

---

#### 🔸 While

`let contador = 0; while (contador < 3) {   console.log("Repetindo...");   contador++; }`

🟢 Executa **enquanto** a condição for verdadeira.

---

#### 🔸 Do...While

`let senha; do {   senha = prompt("Digite sua senha:"); } while (senha !== "1234");`

🟢 Executa **pelo menos uma vez**, mesmo se a condição for falsa inicialmente.

---

#### 🔸 Vetores (Arrays)

`let frutas = ["maçã", "banana", "uva"]; for (let i = 0; i < frutas.length; i++) {   console.log(frutas[i]); }`

🟢 Usa `frutas.length` pra percorrer todos os elementos dinamicamente.

---

### 📚 Dicas de Estudo

- Cria analogias com o dia a dia (ex: “repetir exercícios até acertar”).
    
- Evita loops infinitos → **verifica sempre a condição**!
    
- Usa o **`for...of`** e **`forEach`** pra loops mais modernos e legíveis.
    
- Pratica com vetores de diferentes tipos (números, strings, objetos).
    
- Testa no console e observa o fluxo de execução passo a passo.