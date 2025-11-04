### 💡 Conceito

O **controle de fluxo** define **como o programa toma decisões** com base em condições.  
Ele executa blocos de código diferentes conforme as situações encontradas.

### 🧠 Lembretes

- `if` → verifica uma condição.
    
- `else if` → adiciona novas verificações.
    
- `else` → executa se nenhuma condição for verdadeira.
    
- `switch case` → alternativa mais limpa para vários `if...else`.
    

---

### 🧩 Exemplos Práticos

`let cor = "azul";  if (cor === "vermelho") {   console.log("Cor quente"); } else if (cor === "azul") {   console.log("Cor fria"); } else {   console.log("Cor neutra"); }  // Switch switch (cor) {   case "vermelho":     console.log("Cor quente");     break;   case "azul":     console.log("Cor fria");     break;   default:     console.log("Cor neutra"); }`

---

### 📚 Dicas de Estudo

- Usa exemplos visuais (como semáforos ou cores) pra fixar lógica condicional.
    
- Evita `if` muito aninhados — `switch` deixa o código mais limpo.
    
- Lê as condições em voz alta; ajuda a perceber erros de lógica.
    
- Faz desafios pequenos, tipo calculadoras ou simuladores de notas.