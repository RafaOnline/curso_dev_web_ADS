# Gráficos com Google Charts

**Objetivo**
- Criar uma página que recebe números, adicione em um vetor, e construa o gráfico de linha com a relação **posição** x **valor**

- A página também deverá apresentar a média dos valores que foram inseridos

**Arquivo** `somaVetor.js`
Esse trecho de código JavaScript está criando uma estrutura para:
- Adicionar valores a um vetor com posição e valor.
- Calcular a média dos valores inseridos.
- Desenhar um gráfico de linha usando a biblioteca do Google Charts.
  
```javascript
let valores = []; // Array que armazenará pares [posição, valor]

const addValor = (x) => {
    // Adiciona um novo valor ao array, com a posição sendo o próximo índice
    valores.push([valores.length + 1, x]);
}

const media = () => {
    let soma = 0;
    // Percorre o array e soma os valores (segunda posição de cada par)
    for (let x of valores)
        soma += x[1];
    // Retorna a média dos valores
    return soma / valores.length;
}

const drawBasic = () => {
    // Cria uma nova tabela de dados para o gráfico
    let data = new google.visualization.DataTable();
    data.addColumn('number', 'Pos'); // Coluna para posição
    data.addColumn('number', 'X');   // Coluna para valor

    // Adiciona os dados armazenados no array 'valores'
    data.addRows(valores);

    // Define opções do gráfico
    let options = {
        hAxis: { title: 'Posição' },
        vAxis: { title: 'Valor de X' }
    };

    // Cria e desenha o gráfico de linha no elemento com id 'chart_div'
    let chart = new google.visualization.LineChart(document.getElementById('chart_div'));
    chart.draw(data, options);
}
```

- O usuário digita um valor de X.
- Ao clicar em Executar, o valor é adicionado ao vetor.
- O gráfico é desenhado com os valores acumulados.
- A média dos valores é exibida abaixo do gráfico.

**Arquivo** `ìndex.html`
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <!-- Define o conjunto de caracteres como UTF-8 para suportar acentuação -->

    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Garante que o layout seja responsivo em dispositivos móveis -->

    https://www.gstatic.com/charts/loader.js
    <!-- Carrega a biblioteca do Google Charts -->

    https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css
    <!-- Carrega o CSS do Bootstrap para estilização responsiva -->
</head>
<body class="container">
    <!-- Aplica a classe container do Bootstrap para centralizar o conteúdo -->

    <h1 class="text-center">Google Charts</h1>
    <!-- Título centralizado -->

    <div class="d-flex justify-content-center align-items-center">
        <!-- Centraliza o formulário horizontalmente e verticalmente -->

        <form class="form m-2">
            <!-- Formulário com margem -->

            <label class="fw-bold">Valor de X</label>
            <!-- Rótulo em negrito -->

            <input type="number" id="v1">
            <!-- Campo de entrada numérica com id 'v1' -->

            #Executar</a>
            <!-- Botão que chama a função 'executar()' ao ser clicado -->
        </form>
    </div>

    <div id="chart_div"></div>
    <!-- Área onde o gráfico será desenhado -->

    <div class="alert alert-warning text-center fw-bold" id="media"></div>
    <!-- Área onde será exibida a média dos valores -->

    somaVetor.js</script>
    <!-- Importa o arquivo JavaScript externo que contém as funções addValor, media e drawBasic -->

    <script>
        const executar = () => {
            const x = Number(document.getElementById("v1").value);
            // Lê o valor digitado e converte para número

            addValor(x);
            // Adiciona o valor ao vetor

            google.charts.load('current', {packages: ['corechart', 'line']});
            // Carrega os pacotes necessários do Google Charts

            google.charts.setOnLoadCallback(drawBasic);
            // Quando o Google Charts estiver pronto, chama a função que desenha o gráfico

            document.getElementById("media").innerHTML = `Media: ${media()}`;
            // Atualiza o texto da média com o valor calculado
        }
    </script>
</body>
</html>
```
