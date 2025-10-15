# Introdução ao JavaScript

## Funções no Java Script
Um breve resumo da introdução passada em aula.

Todos os conteúdos que terão nessa unidade foram mostrados resumidamente

```js
  
// Arrow Function

function somar(a, b) {
let somar2 = (a,b) => {
    return a + b;
    }
}
let somar2 = (a, b) => a + b;


// Controle de Fluxo

const numbers = [45, 4, 9, 16, 25];
let txt = "";
for (let x in numbers) {
    txt += numbers[x];
}
const letters = ["a", "b", "c"];
for (const x of letters) {
    txt += x;
}

// vetores

const a = [12, 54, 23];
const b = [99, 30, 45];
let c = a.concat(b);
c.sort();
c.reverse();
c = c.filter ((x) => (x>20 && x<90));

document.getElementById("demo").innerHTML = c.join(" :: ");

//Objetos no Java Script

let Pessoa = [{idade: 25, nome:"Ana"},
    {idade: 43, nome: "Carlos"}];

function Pessoa(nome, idade){
    this.none = nome; this.idade = idade;
}
let Pessoa = [new Pessoa("Ana",25), 
    new Pessoa ("Carlos", 43)];
```
