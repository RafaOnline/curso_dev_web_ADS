# Composição e Criação de Vetores

## Definição e Manipulação de Vetores
- Baseados na classe **Array**
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

### Geração de texto com Join
- Insere String a cada número no vetor
- O resultado é transformado em Strings
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
</head>
<body>
    <script>
        const valores = [1, 3, 4, 7, 8];
        const saida = valores.join("::");
        console.log(saida);
    </script>
</body>
</html>
```

Resultado:

<img width="552" height="207" alt="image" src="https://github.com/user-attachments/assets/46718c45-e01f-4f7c-a9ec-15a6ee082f92" />

### Ordenação, Mapeamento e Redução

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo com Array e Funções</title>
</head>

<body>
    <!-- Botão que executa a função "executar" quando clicado -->
    <button onclick="executar()">Clique aqui</button>

    <script>
        // Função arrow chamada quando o botão é clicado
        executar = () => {
            // Cria um array com números
            const valores = [1, 6, 5, 9, 2];

            // Ordena o array em ordem alfabética (por padrão, sort converte para string)
            // Exemplo: [1, 2, 5, 6, 9] — nesse caso funciona, mas em números grandes pode dar erro
            valores.sort();

            // Exibe o array ordenado no console
            console.log(valores);

            // Exibe o valor que está na posição 3 do array (lembrando que o índice começa em 0)
            console.log(`Valores na posição 3: ${valores[3]}`);

            // Percorre o array e mostra cada elemento com seu índice
            valores.forEach((element, index) => console.log(`Valor[${index}]: ${element}`));

            // Cria um novo array com todos os valores dobrados e soma tudo
            // .map() → multiplica cada elemento por 2
            // .reduce() → soma todos os elementos resultantes
            const somaDobro = valores.map((e) => e * 2).reduce((a, b) => a + b);

            // Exibe o resultado final no console
            console.log("Soma 2x = " + somaDobro);
        }
    </script>
</body>

</html>

```

Resultado:

<img width="552" height="176" alt="image" src="https://github.com/user-attachments/assets/fddf4c1c-f085-4834-8bfc-c4452eb5b918" />

### Exemplo com randômicos
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <!-- Cria uma tabela que ocupa 100% da largura da página -->
    <table style="width: 100%;">
        <script>
            // Define um array com três cores
            const cores = ["red", "green", "blue"];

            // Loop externo para criar 9 linhas na tabela
            for (let i = 1; i < 10; i++) {
                document.write("<tr>"); // Inicia uma nova linha da tabela

                // Loop interno para criar 9 células por linha
                for (let i = 1; i < 10; i++) {
                    // Gera um número aleatório entre 0 e 2 para escolher uma cor
                    let pos = Math.trunc(Math.random() * 3);

                    // Escreve uma célula com a cor de fundo aleatória
                    document.write(`<td style='background-color:${cores[pos]}'>&nbsp;</td>`);
                }

                document.write("</tr>"); // Fecha a linha da tabela
            }
        </script>
    </table>
</body>
</html>
```

Resultado: 

Cada vez que recarregar a página exibe um resultado aleatório.

<img width="676" height="197" alt="image" src="https://github.com/user-attachments/assets/90036bb8-b096-407d-9d08-751b7371eb70" />

### Matrizes, Vetores e Método flat

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <!-- Define o conjunto de caracteres como UTF-8 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Garante que o layout seja responsivo em dispositivos móveis -->
</head>
<body>
    <script>
        // Cria uma matriz (array de arrays) com 3 linhas e 2 colunas
        const matriz = [[1, 2], [3, 4], [5, 6]];

        // Exibe a matriz original no console
        console.log(matriz);

        // Usa o método flat() para "achatar" a matriz em um vetor simples
        const vetor = matriz.flat();

        // Exibe o vetor resultante no console
        console.log(vetor);
    </script>
</body>
</html>
```
**O que o código faz:**
- Cria uma matriz 2D com os valores [[1, 2], [3, 4], [5, 6]].
- Usa o método .flat() para transformar essa matriz em um vetor 1D: [1, 2, 3, 4, 5, 6].
- Mostra os dois no console para comparação.

Resulado:

<img width="540" height="241" alt="image" src="https://github.com/user-attachments/assets/867bcc5b-3fe8-4c55-9a73-a4adcf90fc15" />


