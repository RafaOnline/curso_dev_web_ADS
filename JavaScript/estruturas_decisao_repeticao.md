# Estruturas de decisão e de repetição
---
## Estruturas condicionais em JavaScript

### Comando `IF` - Estrutura Se/Então
- Comandos são executados apenas se a condição for verdadeira
- Para mais uma instrução, é obrigatório delimitar o bloco com chaves, mas para uma instrução intrução simples as chaves são opcionais.

```javascript
let a = eval(prompt("Numero: "));
if(a%2 == 0){
    alert("O número é par");
    console.log(`Valor &{a}`);
}
```

---

### Operadores Relacionais
Caracteristicas Gerais:
- Tem como entrada dois valores númericos e como saida um valor booleano
- Aceita variáveis e instruções aritméticas
```javascript
const b = 10, c = 5;
let w;

// Com aritmética
let f = (x + 2) < Math.pow(x , 3);
```


| Instrução | Resultado |
|:---------:|:---------:|
| w = a > b; | 🟩 True |
| w = a < b; | 🟥 False |
| w = a == b; | 🟥 False |
| w = a != b; | 🟩 True |
| w = a >= b; |🟩 True |
| w = a <= b; | 🟥 False |
