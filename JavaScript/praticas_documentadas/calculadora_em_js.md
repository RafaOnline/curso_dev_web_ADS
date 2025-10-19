# javaScript na prática

## Calculadora Simples

Este é um projeto de uma calculadora simples desenvolvida com HTML, CSS e JavaScript com interface que utiliza o framework **Bootstrap** para estilização responsiva e moderna.
A calculadora permite realizar operações básicas como soma, subtração, multiplicação, divisão e exponenciação.

## Funcionalidades

- Soma
- Subtração
- Multiplicação
- Divisão (com verificação de divisão por zero)
- Potência

## Estrutura do Projeto

### `index.html`
Arquivo principal que define a estrutura da interface da calculadora. Utiliza Bootstrap para estilização e contém campos para entrada de valores, seleção de operação e exibição do resultado.

```html
<!DOCTYPE html>
<html lang="pt-BR">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora Simples</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.1.3/dist/css/bootstrap.min.css"
        integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
    <link rel="stylesheet" type="text/css" href="style.css">
</head>

<body>


    <div class="container container-tamanho border border-dark ">
        <h1 class="text-center p-2" >Calculadora</h1>
        <form class="form m-2">
            <div class="form-group">
                <label class="form-label" for="valor_1">Valor A</label>
                <input class="form-control" type="number" name="valor_1" id="valor_1">
            </div>

            <div class="form-group">
                <label class="form-label" for="valor_2">Valor B</label>
                <input class="form-control" type="number" name="valor_2" id="valor_2">
            </div>

            <div class="form-group">
                <label for="operacao">Operação</label>
                <select class="form-control" name="operacao" id="operacao">
                    <option disabled selected>Selecione</option>
                    <option>Soma</option>
                    <option>Subtração</option>
                    <option>Multiplicação</option>
                    <option>Divisão</option>
                    <option>Potência</option>
                </select>
            </div>

            <div class="row justify-content-center">
                <a href="#" class="btn btn-primary" onclick="executar()">Executar</a>
            </div>

        </form>

        <div class="alert alert-success d-none" role="alert" id="resposta"></div>

        <script src="calculadora.js"></script>
        <script>
            const executar = () => {
                const a = eval(document.getElementById("valor_1").value);
                const b = eval(document.getElementById("valor_2").value);
                let operacao = eval(document.getElementById("operacao").selectedIndex);
                if (isNaN(a) || isNaN(b) || document.getElementById("operacao").selectedIndex === 0) {
                    resposta.className = "alert alert-warning mt-3";
                    resposta.innerHTML = "⚠️ Por favor, preencha todos os campos corretamente.";
                    return;
                }
                let resultado = (operacao == 1) ? somar(a, b) : (operacao == 2) ? subtrair(a, b) : (operacao == 3) ? multiplicar(a, b) : (operacao == 4) ? dividir(a, b) : exponencial(a, b);
                document.getElementById("resposta").innerHTML = `O resultado da operação é ${resultado}`;
                resposta.classList.remove("d-none");
            }
        </script>
    </div>

</body>

</html>
```

### `calculadora.js`
Contém as funções responsáveis pelas operações matemáticas:

```javascript
function somar(a,b){ return a+b; }
function subtrair(a,b){ return a-b; }
function multiplicar(a,b){ return a*b; }
function dividir(a,b){
    if(b==0)
        alert("Divisão por Zero!!!!")
    return a/b;
}
function exponencial(a,b){ return Math.pow(a,b); }
```

### `style.css`
Define o estilo personalizado da calculadora, como o tamanho do container e o espaçamento:

```css
.container-tamanho {
    width: 300px;
    margin-top: 150px;
}
```

## Como Usar

1. Abra o arquivo `index.html` em um navegador.
2. Insira os valores nos campos "Valor A" e "Valor B".
3. Selecione a operação desejada.
4. Clique em "Executar" para ver o resultado.

## Observações

- O projeto utiliza `eval()` para obter os valores dos campos, o que pode representar riscos de segurança em aplicações reais. Para produção, recomenda-se evitar o uso de `eval()`.
- A verificação de divisão por zero exibe um alerta ao usuário.


