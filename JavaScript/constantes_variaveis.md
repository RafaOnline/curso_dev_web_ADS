# Definição de Constantes e Variáveis

# Tipagem Fraca
- O tipo é definido pela atribuição corrente para a variável
- Uma simples atribuição define a variável
- A palavra var era utilizada para definir uma variável formalmente
- Hoje temos **let**, para valores que podem ser alterados, e **const**, para valores fixos.

Exemplo:
```js
let a = 10; // Varíavel que pode ser alterada
const nome = "Rafael"; // Variável que não pode ser alterada
```

## Tipo de Operadores

- Aritméticos: + - * / %
- Lógico e Binários: && || ! | & ^
- Relacionais: >= === != <= > <
- Concatenação: + ${}
- Decisão: ?

  ```js
  let b1 = (z > c) && (c <= d);
  let texto = (z >= 5) ? "APR" : "RPR;
  let k = 5 ^ 2: 
  ```

## Classes e Objetos

Definição de **Classes**:  Classes em JavaScript são uma forma de organizar e estruturar código orientado a objetos. Elas permitem criar modelos (ou "moldes") para objetos, agrupando dados (propriedades) e comportamentos (métodos) relacionados.
  

```js
// Sintaxe nova
class Pessoa {
    constructor(nome,idade){
        this.nome = nome; this.idade = idade;
    }
    exibir = () => console.log(`${this.nome} ${this.idade}`);
};


// Criando uma instância da classe
const pessoa1 = new Pessoa("Rafael", 30);

// Chamando o método exibir
pessoa1.exibir();
```
```js
// Sintaxe antiga
function Pessoa(nome, idade){
    this.nome = nome;  this.idade = idade;
    this.exibir = () => console.log(`${this.nome} ${this.idade}`);
};

const teste = new Pessoa("Rafael", 30);

teste.exibir();
```
