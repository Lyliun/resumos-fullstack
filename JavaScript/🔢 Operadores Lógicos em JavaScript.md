### 💡 Conceito

Os **operadores lógicos** permitem combinar ou inverter condições.  
Eles retornam sempre um valor **booleano** (`true` ou `false`) e são muito usados em **estruturas condicionais**.

### 🧠 Lembretes

- `&&` → **E lógico** (true só se as duas forem verdadeiras).
    
- `||` → **OU lógico** (true se pelo menos uma for verdadeira).
    
- `!` → **NÃO lógico** (inverte o resultado da condição).
    
- Sempre usados dentro de expressões condicionais com `if`, `while`, etc.
    

---

### 🧩 Exemplos Práticos

`let idade = 20; let possuiCarteira = true;  // Exemplo de E lógico if (idade >= 18 && possuiCarteira) {   console.log("Pode dirigir"); }  // Exemplo de OU lógico if (idade < 18 || !possuiCarteira) {   console.log("Não pode dirigir"); }`

---

### 📚 Dicas de Estudo

- Monta tabelas verdade para entender cada operador.
    
- Testa condições diferentes e observa os resultados.
    
- Treina misturar operadores (`&&`, `||`, `!`) em expressões mais complexas.
    
- Usa exemplos reais — como permissões de login, acesso a conteúdos, etc.