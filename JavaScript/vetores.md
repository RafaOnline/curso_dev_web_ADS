# Composição e Criação de Vetores

## Definição e Manipulação de Vetores
- Baseados na classe **Array*
- Métodos na ordenação **sort**
- Iteração através de **forEach**
- Métodos **map** e **reduce**

Exemplo:
```js
valores = [1,6,5,9,2];
// Ou também pode ser definido como: valores = new Array(1,6,5,9,2);
valores.sort();
console.log(valores);
console.log(`Valor na posição 3: ${valores[3]}`);
```

### Definição de vetores
- Vetores são sequências de elementos de um mesmo tipo
- No JavaScript eles funcionam como listas
- Podem ser definidos com colchete, ou com base na classe Array

```javascript
let cores1 = ["red", "blue","green"];
let cores2 = new Array("red", "blue", "green");

let vazio1 = [];
let vazio2 = new Array();
```

### Acesso
- Acessos aos elementos através do índice
- O primeiro índice tem valor zero
```javascript
console.log(cores[2]); //imprime green
document.getElementById("demo").style.color = cores2[1]; //define fonte azul
```
