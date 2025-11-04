### 💡 Conceito

**Persistência de dados** significa armazenar informações de forma que **não se percam quando o programa encerra**.  
É o que permite salvar usuários, configurações ou históricos.

### 🧠 Lembretes

- Em JavaScript, pode ser feita com:
    
    - **LocalStorage / SessionStorage** (no navegador).
        
    - **Bancos de dados** (MySQL, MongoDB, PostgreSQL, etc.) no backend.
        
- Dados persistentes são armazenados de forma **não volátil** (continuam lá mesmo após reiniciar o sistema).
    

---

### 🧩 Exemplos Práticos

``// Salvando dados no navegador localStorage.setItem("usuario", "Lia");  // Recuperando o valor let nome = localStorage.getItem("usuario"); console.log(`Bem-vinda de volta, ${nome}!`);``

---

### 📚 Dicas de Estudo

- Entende a diferença entre **armazenamento local** e **banco de dados**.
    
- Aprende os conceitos de **CRUD** (Create, Read, Update, Delete).
    
- Experimenta usar **APIs + bancos de dados** pra guardar informações reais.
    
- Observa como aplicações modernas mantêm o estado mesmo após o reload.