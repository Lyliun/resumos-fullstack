
### 💡 Conceito

**Getters e Setters** são **métodos especiais** usados pra **ler e alterar valores privados** de uma classe, respeitando o **encapsulamento**.

Em TypeScript:

- `get` → permite acessar uma propriedade privada como se fosse pública.
    
- `set` → define ou altera o valor dessa propriedade com controle adicional.

### ⚙️ **Exemplo Prático**

`class ContaBancaria {   private _saldo: number = 0;    get saldo(): number {     return this._saldo;   }    set saldo(valor: number) {     if (valor < 0) {       console.log("Valor inválido!");     } else {       this._saldo = valor;     }   } }  const conta = new ContaBancaria(); conta.saldo = 100; // usa o setter console.log(conta.saldo); // usa o getter → 100`

---

### 🧭 **Lembretes**

- Sempre usa nomes claros para atributos privados (`_atributo` é uma convenção comum).
    
- Getters e Setters ajudam a evitar acesso direto a propriedades sensíveis.
    
- Evita usar `set` pra cálculos complexos — mantenha o foco no controle de acesso.
    

---

### ✨ **Dicas de Estudo**

- Experimenta quebrar o código propositalmente pra entender os erros de acesso a `private`.
    
- Faz analogia com cofres: o getter é a janelinha pra ver o saldo, o setter é a chave pra alterar.