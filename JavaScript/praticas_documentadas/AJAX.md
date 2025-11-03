# Utilização do AJAX com XMLHttpResquest
**Objetivo**
- Testar a utilização do XMLHttpResquest através de uma chamada GET para a **httpbin.org**
- Essa API gratuita retorna os dados da solicitação HTTP efetuada.

### Arquivo `ajax.js`
```javascript
// Função chamada 'ajax' que recebe dois parâmetros: 'nome' e 'camada'
function ajax(nome, camada) {
    // Monta a URL para a requisição GET, incluindo o parâmetro 'text' com o valor de 'nome'
    var url = 'https://httpbin.org/get?text=' + nome;

    // Cria um novo objeto XMLHttpRequest para fazer a requisição HTTP
    var xmlhttp = new XMLHttpRequest();

    // Define a função que será chamada sempre que o estado da requisição mudar
    xmlhttp.onreadystatechange = function() {
        // Verifica se a requisição foi concluída (readyState == 4) e se foi bem-sucedida (status == 200)
        if (xmlhttp.readyState == 4 && xmlhttp.status == 200) {
            // Armazena a resposta da requisição na variável 'resp'
            var resp = xmlhttp.responseText;

            // Insere o conteúdo da resposta dentro do elemento HTML com o ID igual ao valor de 'camada'
            document.getElementById(camada).innerHTML = resp;
        }
    }

    // Inicializa a requisição GET com a URL montada, de forma assíncrona (true)
    xmlhttp.open("GET", url, true);

    // Envia a requisição para o servidor
    xmlhttp.send();
}
```
### Aquivo `index.html`
```html
<body>
    <!-- Título principal da página -->
    <h1>API de Testes httpbin</h1>

    <!-- Formulário com um campo de texto para entrada do nome -->
    <form>
        <!-- Rótulo para o campo de entrada de texto -->
        <label for="n1">Nome</label>

        <!-- Campo de entrada de texto com id "n1" -->
        <input type="text" id="n1">

        <!-- Link que, ao ser clicado, executa a função "executar()" -->
        #Executar</a>
    </form>

    <!-- Div onde será exibido o retorno da requisição AJAX -->
    <div id="retorno"></div>

    <!-- Importação de um script externo chamado "ajax.js" -->
    ajax.js</script>

    <!-- Script interno que define a função "executar" -->
    <script>
        // Função que será chamada ao clicar no link "Executar"
        const executar = () => {
            // Obtém o valor digitado no campo de texto com id "n1"
            const nome = document.getElementById("n1").value;

            // Chama a função "ajax" definida no arquivo "ajax.js", passando o nome e o id da div de retorno
            ajax(nome, "retorno");
        }
    </script>
</body>
```

### 📌 Resumo da funcionalidade dos dois arquivos juntos
Esses dois arquivos juntos criam uma pequena aplicação web que:
- Permite ao usuário digitar um nome.
- Ao clicar em "Executar", envia esse nome como parâmetro para a API pública https://httpbin.org usando AJAX.
- A resposta da API (em formato JSON) é exibida diretamente na página, dentro da `<div id="retorno">`, sem recarregar a página.
É uma ótima base para aprender sobre requisições assíncronas e manipulação de DOM com JavaScript puro.
