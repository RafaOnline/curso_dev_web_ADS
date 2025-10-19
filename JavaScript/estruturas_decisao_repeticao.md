# Estruturas de decisão e de repetição
---
## Estruturas condicionais em JavaScript

### Comando `IF` - Estrutura Se/Então
- Comandos são executados apenas se a condição for verdadeira
- Para mais uma instrução, é obrigatório delimitar o bloco com chaves, mas para uma instrução intrução simples as chaves são opcionais.

```javascript
// Declaração de constantes
const b = 10, c = 5; // b e c são constantes com valores fixos

// Declaração de variável
let w; // w é uma variável que pode ser usada posteriormente

// Expressão com aritmética e comparação
// Aqui, 'f' será verdadeiro se (x + 2) for menor que x elevado à 3ª potência
let f = (x + 2) < Math.pow(x, 3);

// Explicação:
// - (x + 2): soma 2 ao valor de x
// - Math.pow(x, 3): calcula x³ (x elevado à terceira potência)
// - O operador '<' compara se o resultado da soma é menor que o resultado da exponenciação
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

---

### Operadores Lógicos
Características gerais
- Tem como entrada dois valores booleanos e como saída um valor booleano
- Permite combinar operações relacionais
- Curto-circuito minimiza comparações

```javascript
let f = (x <= 2) && ( y != 3);
```

Exemplos:
- Se x = 1 e y = 4 → f = true
- Se x = 3 e y = 4 → f = false (porque x <= 2 é falso)
- Se x = 2 e y = 3 → f = false (porque y != 3 é falso)

  ---
  
