# Estruturas de decisão e de repetição
---

### Comando `IF` - Estrutura Se/Então
- Comandos são executados apenas se a condição for verdadeira
- Para mais uma instrução, é obrigatório delimitar o bloco com chaves, mas para uma instrução intrução simples as chaves são opcionais.

Exemplos:
```javascript
// Solicita ao usuário que digite um número
let a = eval(prompt("Número: "));

// Verifica se o número é par usando o operador módulo (%)
// Se o resto da divisão por 2 for zero, o número é par
if (a % 2 == 0) {
    // Exibe um alerta informando que o número é par
    alert("O número é par");

    // Exibe o valor digitado no console
    console.log(`Valor: ${a}`);
}
```


```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo estrutura IF</title>
</head>
<body>
    <h2>Estrutura IF</h2>
    <p>Apresenta "Bom dia" se for menos que 12:00</p>
    <p id="demo">Já passou de meio-dia</p>

    <script>
        // Obtém a hora atual do sistema
        let horaAtual = new Date().getHours();

        // Verifica se a hora é menor que 12 (meio-dia)
        if (horaAtual < 12) {
            // Se for antes do meio-dia, altera o conteúdo do parágrafo com id "demo"
            document.getElementById("demo").innerHTML = "Bom dia";
        }
        // Caso contrário, o texto "Já passou de meio-dia" permanece
    </script>
</body>
</html>
```

---

### Operadores Relacionais
Caracteristicas Gerais:
- Tem como entrada dois valores númericos e como saida um valor booleano
- Aceita variáveis e instruções aritméticas
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

  ### Comando `IF` `ELSE` - Estrutura Se/Então/Senão
  - Comandos diferentes executados para cada resultado da condição(verdadeira ou falsa)
  - Para mais de uma instrução, é obrigatório delimitar o bloco com chaves, mas para uma intrução simples as chaves são opcionais.
 
```javascript
  // Solicita ao usuário que digite um número
let a = eval(prompt("Número: "));

// Verifica se o número é par ou ímpar
if (a % 2 == 0) {
    // Se o número for par, exibe uma mensagem de alerta
    alert("O número é par");
} else {
    // Se o número for ímpar, exibe uma mensagem de alerta
    alert("O número é ímpar");
}
```

Estrutua if else aninhada

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h2>Estrutura if else if</h2>
    <p>Modifica o comprimento de acordo com a hora do dia</p>
    <p id="demo">Que horas são?</p>
    <script>
        let painel = document.getElementById("demo");
        let hora = new Date().getHours();
        if (hora < 12){painel.innerHTML = "Bom dia!";}
        else if (hora < 18){painel.innerHTML = "Boa tarde";}
        else{painel.innerHTML = "Boa noite!";}

        // Exemplo usando Operador de Decisão

        let painel1 = document.getElementById("demo");
        let hora2 = new Date().getHours();
        painel.innerHTML = 
        (hora < 12) ? "Bom dia!":
        (hora < 18) ? "Boa tarde!":
                        "Boa noite!";
    </script>
</body>
</html>
```

Operadores lógicos
```javascript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Saudação com Operador Ternário</title>
</head>
<body>
    <h2>Estrutura if else if com operador ternário</h2>
    <p>Modifica a saudação de acordo com a hora do dia</p>
    <p id="demo">Que horas são?</p>

    <script>
        // Obtém o elemento HTML com id "demo"
        let painel = document.getElementById("demo");

        // Obtém a hora atual do sistema (0 a 23)
        let hora = new Date().getHours();

        // Usa operador ternário para definir a saudação com base na hora
        // Se hora < 12 → "Bom dia!"
        // Se hora < 18 → "Boa tarde!"
        // Caso contrário → "Boa noite!"
        painel.innerHTML = 
            (hora < 12) ? "Bom dia!" :
            (hora < 18) ? "Boa tarde!" :
                             </script>
</body>
</html>
```
Comando Swtich 
```javascript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Verificador de Par ou Ímpar</title>
</head>
<body>
    <script>
        // Inicializa a variável 'frase' como string vazia
        let frase = "";

        // Solicita ao usuário que digite um valor e converte para número usando eval
        let b = eval(prompt("Valor"));

        // Usa a estrutura switch para verificar se o número é par ou ímpar
        switch (b % 2) {
            case 0:
                // Se o resto da divisão por 2 for 0, o número é par
                frase = "O número é par";
                break;
            case 1:
                // Se o resto da divisão por 2 for 1, o número é ímpar
                Exibe a mensagem correspondente em uma caixa de alerta
                frase = "O número é ímpar";
                break;
        alert(frase);
    </script>
</body>
</html>
```
  
