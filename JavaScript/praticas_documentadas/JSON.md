# JSON na Prática 
### Teste de utilização de JSON e fetch com API Gratuita
**Objetivo**
- Testar a utilização de JSON e fetch com base em uma chamada GET para a **randomuser.me**
- Essa API gratuita retorna dados de usuários aleatórios no formato JSON

### Arquivo `json.js`
```javascript
// Define a URL da API que retorna dados de usuários aleatórios
const url = `https://randomuser.me/api/?results=10`;

// Função assíncrona que busca os usuários e atualiza a lista no HTML
async function getUsers(lista){
    // Faz a requisição para a API usando fetch
    const resp = await fetch(url);

    // Converte a resposta em JSON
    const objeto = await resp.json();

    // Inicializa uma string vazia para armazenar os itens da lista
    let itens = "";

    // Percorre cada pessoa retornada pela API
    for (let pessoa of objeto.results){
        // Adiciona o nome da pessoa como item de lista (li), usando nome e sobrenome
        itens += `<li>${pessoa.name.first} ${pessoa.name.last}</li>`;
    }

    // Insere os itens gerados dentro do elemento HTML com o ID passado como parâmetro
    document.getElementById(lista).innerHTML = itens;
}
```

### Arquivo `index.html`
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>

<body>
    <!-- Título principal da página -->
    <h1>API de Testes randomusers</h1>

    <!-- Link que, ao ser clicado, executa a função 'executar' -->
    <a href="#" onclick="executar()">Executomes dos usuários serão exibidos -->
    <ul id="retorno"></ul>

    <!-- Importa o arquivo JavaScript externo que contém a função getUsers -->
    <script src="json.js"></script>

 interno que define a função 'executar' e chama getUsers -->
    <script>
        // Função que chama getUsers passando o ID da lista como parâmetro
        const executar = () => {
            getUsers("retorno");
        }
    </script>

</body>

</html>
```

### ✅ Resumo da funcionalidade
O conjunto dos dois arquivos (HTML + JS) cria uma página simples que, ao clicar no link "Executar", 
faz uma requisição à API https://randomuser.me para obter 10 usuários aleatórios. 
Os nomes desses usuários são exibidos em uma lista (`<ul>`) na página.


Resultado:

<img width="355" height="274" alt="image" src="https://github.com/user-attachments/assets/ec67bb3f-23f4-4a77-8bdb-a82d92eeac8a" />

Sempre ao clicar e executar a API trás 10 nomes diferentes.
