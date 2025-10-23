# Série de Fibonacci

**Objetivo**
- Imprimir os números da Série de Fibonacci, a partir da posição 0 até X, fornecido pelo usuário

**F(0) = 1**

**F(1) = 1**

**F(N) = F(N-1) + F(N-2)**, para N > 1

arquivo `fibo.js`
```javascript
// Função iterativa para calcular o número de Fibonacci na posição x
const fibonacci = (x) => {
    // Caso base: se x for 0 ou 1, retorna 1
    if (x == 0 || x == 1)
        return 1;

    // Inicializa os dois primeiros números da sequência
    let fm1 = 1, fm2 = 1, fm;

    // Loop para calcular o número de Fibonacci até a posição x
    for (let i = 1; i <= x; i++) {
        fm = fm1 + fm2; // Soma dos dois anteriores
        fm2 = fm1;      // Atualiza fm2 para o valor anterior de fm1
        fm1 = fm;       // Atualiza fm1 para o novo valor calculado
    }

    // Retorna o número de Fibonacci na posição x
    return fm;
}

// Função recursiva para calcular o número de Fibonacci na posição x
const fiboRec = (x) => {
    // Caso base: se x for 0 ou 1, retorna 1
    // Caso contrário, chama a função recursivamente para x-1 e x-2
    return (x == 0 || x == 1) ? 1 : (fiboRec(x - 1) + fiboRec(x - 2));
}
```

arquivo `fibonacci.html`
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Define a codificação de caracteres e a escala da visualização para dispositivos móveis -->
</head>
<body>
    <h1>Série de Fibonacci</h1>

    <!-- Formulário para entrada do valor de X -->
    <form>
        <label>Valor de X</label>
        <input type="number" id="v1"> <!-- Campo para o usuário digitar o valor de X -->
        <a href="#" onclick="executar()">Executar</a> <!-- Link que chama a função executar() ao ser clicado -->
o resultado será exibido -->
    <div id="resp">O resultado aparece aqui</div>

    <!-- Importa o arquivo JavaScript externo que contém a função fibonacci -->
    fibo.js</script>

    <!-- Script interno que executa a lógica ao clicar em "Executar" -->
    <script>
        const executar = () =>            // Obtém o valor digitado pelo usuário e avalia como número
            const x = eval(document.getElementById("v1").value);

            // Inicializa a variável da série e o contador
            let serie = "", i = 0;

            // Gera a série de Fibonacci até o valor de X
            while (i <= x) {
                serie += fibonacci(i) + " "; // Adiciona o número à série
                i++;
            }

            // Exibe o resultado na div com id "resp"
            document.getElementById("resp").innerHTML = `Resultado: ${serie}`;
        }
    </script>
</body>
</html>
```
