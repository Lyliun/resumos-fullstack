
### 💡 **Conceito**

O **construtor** é um **método especial** dentro de uma classe que é **executado automaticamente** quando um **objeto é criado**.  
Ele serve para **inicializar os atributos** da classe e **garantir que o objeto comece com valores definidos**.

Em outras palavras: o construtor “monta” o objeto no momento em que ele nasce.

### ⚙️ **Estrutura Básica em TypeScript**

``class Pessoa {   nome: string;   idade: number;    constructor(nome: string, idade: number) {     this.nome = nome;     this.idade = idade;   }    apresentar(): void {     console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);   } }  const lia = new Pessoa("Lia", 21); lia.apresentar();``

🔹 **`constructor()`** é o nome fixo do método construtor.  
🔹 Pode receber **parâmetros** para definir os valores iniciais.  
🔹 O `this` faz referência ao **objeto atual**, ou seja, a instância que está sendo criada.

---

### 🧠 **Regras Importantes**

- Cada classe pode ter **apenas um construtor**.
    
- Se nenhum for declarado, o TypeScript cria **um construtor padrão vazio** automaticamente.
    
- Pode usar **valores padrão** nos parâmetros.
    
- Pode chamar o **construtor da classe pai** com `super()` (em casos de herança).
    

---

### 🧩 **Exemplo com Valores Padrão**

``class Carro {   marca: string;   ano: number;    constructor(marca: string = "Desconhecida", ano: number = 2020) {     this.marca = marca;     this.ano = ano;   }    mostrarInfo(): void {     console.log(`Carro: ${this.marca}, Ano: ${this.ano}`);   } }  const carro1 = new Carro("Fiat", 2022); const carro2 = new Carro();  carro1.mostrarInfo(); // Carro: Fiat, Ano: 2022 carro2.mostrarInfo(); // Carro: Desconhecida, Ano: 2020``

---

### 🧬 **Construtor com Herança (Uso de `super()`)**

``class Animal {   nome: string;    constructor(nome: string) {     this.nome = nome;   } }  class Cachorro extends Animal {   raca: string;    constructor(nome: string, raca: string) {     super(nome); // chama o construtor da classe pai     this.raca = raca;   }    latir(): void {     console.log(`${this.nome}, da raça ${this.raca}, está latindo!`);   } }  const dog = new Cachorro("Bolt", "Vira-lata"); dog.latir();``

🔸 `super()` **deve ser chamado antes** de acessar `this` na subclasse.  
🔸 Garante que o construtor da classe pai execute sua parte da inicialização.

---

### 🧭 **Lembretes**

- O construtor é o **primeiro método executado** quando o objeto nasce.
    
- Ele **não retorna valores** (nem precisa de `return`).
    
- Pode ser usado para **validar dados iniciais** antes de criar o objeto.
    
- O **encapsulamento** pode ser usado junto (por exemplo, usando `private` nos atributos).
    

---

### 🧩 **Exemplo com Validação Interna**

``class ContaBancaria {   titular: string;   saldo: number;    constructor(titular: string, saldoInicial: number) {     this.titular = titular;     this.saldo = saldoInicial >= 0 ? saldoInicial : 0;   }    mostrarSaldo(): void {     console.log(`Saldo atual de ${this.titular}: R$${this.saldo}`);   } }  const conta = new ContaBancaria("Lia", -50); conta.mostrarSaldo(); // Saldo atual de Lia: R$0``

---

### ✨ **Dicas de Estudo**

- Cria classes simples e tenta passar diferentes tipos de parâmetros no construtor.
    
- Faz o exercício de herança — cria uma classe pai e outra filha usando `super()`.
    
- Usa valores padrão pra entender como evitar erros de inicialização.
    
- Lembra: construtor = **porta de entrada dos dados do objeto**.
    

---

### 🌸 **Resumo Final**

> O **construtor** é o método que **dá vida ao objeto** no momento em que ele é criado.  
> Ele garante que todos os atributos sejam **inicializados corretamente**, mantendo o código **organizado, seguro e coerente**.