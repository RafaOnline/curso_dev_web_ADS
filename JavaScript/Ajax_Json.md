# Ajax e Json
---
### Requisições assíncromas em JavaScript
**AJAX - Http Assíncrono, JavaScript e XML**
- Http é um protocolo síncrono, mas o use de XmlHttpRequest permite criar clientes assíncronos
- Atualmente temos outras opções como: fetch, RxJS e Axios
- Apesar de ser utilizado inicialmente com XML, permite formatos como texto simples e JSON
- Viabiliza a construção de páginas com carregamento dinâmico

### Formato JSON (Java Script Object Notation)
- Formato simples para definição de objetos em JavaScript
- As propriedades do objeto são definidos na forma atributo:valor e separados com vírgula
- Um objeto é definido com o uso de chaves
- Vetores são criados com colchetes
- Permite definição hierárquica

**Exemplo de JSON**
```json
// JSON com texto
{"name":"Jonh","idade":25}
```
```javascript
// JSON com JavaScript
{name:"John",idade:25}
```

### Chamada HTTP com XmlHtppResquest
🧠 O que esse código faz:
- Esse trecho de código JavaScript utiliza a API XMLHttpRequest para fazer uma requisição HTTP assíncrona.
- Faz uma requisição GET para um endereço (por exemplo, um arquivo .txt, .html, ou uma API).
Quando a resposta chega com sucesso, insere o conteúdo no elemento HTML com id="demo".
```javascript
let xhttp = new XMLHttpRequest();
xhttp.onreadystatechange = function(){
    if(this.readyState == 4 && this.status == 200){
        document.getElementById("demo").innerHTML = xhttp.responseText;
    }
};
xhttp.open("GET","endereço", true);
xhttp.send();
```
