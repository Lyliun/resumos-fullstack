### 💡 Conceito

A **Programação Orientada a Objetos (POO)** é um paradigma de programação baseado na ideia de organizar o código em **objetos**, que representam entidades do mundo real e possuem **propriedades (atributos)** e **ações (métodos)**.

Em TypeScript, a POO é fortemente apoiada por causa do seu sistema de **tipagem estática** e **classes** modernas do ECMAScript.

### 🧠 **Pilares da POO**

1. **Abstração** — Simplificar a complexidade, focando apenas nos detalhes importantes.  
    _Exemplo:_ uma classe `Carro` mostra só o necessário (métodos como `acelerar()`, `frear()`), sem revelar como o motor funciona internamente.
    
2. **Encapsulamento** — Proteger os dados, controlando o acesso a propriedades internas.  
    _Exemplo:_ usar `private`, `protected` e `public` para definir o que pode ser acessado de fora da classe.
    
3. **Herança** — Reutilizar código criando classes-filhas que herdam características da classe-pai.  
    _Exemplo:_ `class Cachorro extends Animal {}` herda propriedades de `Animal`.
    
4. **Polimorfismo** — Permitir que métodos com o mesmo nome se comportem de maneiras diferentes dependendo do contexto.  
    _Exemplo:_ `emitirSom()` pode fazer um cachorro latir e um gato miar.
    

---

### ⚙️ **Exemplo Prático**

`class Animal {   constructor(public nome: string) {}    emitirSom(): void {     console.log("Som genérico de animal");   } }  class Cachorro extends Animal {   emitirSom(): void {     console.log("Au au!");   } }  const rex = new Cachorro("Rex"); rex.emitirSom(); // Saída: Au au!`

---

### 🧭 **Lembretes**

- Em TypeScript, o uso de **modificadores de acesso** (`public`, `private`, `protected`) é essencial pra definir o encapsulamento.
    
- `constructor` é um método especial usado pra inicializar objetos da classe.
    
- Classes podem **implementar interfaces** e **estender outras classes**.
    

---

### ✨ **Dicas de Estudo**

- Pensa em classes como “moldes” de objetos — tudo que pertence a uma entidade deve estar dentro dela.
    
- Reescreve exemplos simples de POO em TypeScript e JavaScript pra fixar as diferenças.
    
- Desenha o diagrama de classes no caderno — ajuda a visualizar relações de herança e composição.