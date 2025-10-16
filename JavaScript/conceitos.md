# Conceitos e sintaxe do JavaScript

## Árvore DOM(document object model)
Interpretação das **TAGS** de forma **Hierárquica**

<img width="500" height="783" alt="image" src="https://github.com/user-attachments/assets/a745f4a1-95d9-43c4-98e3-46ca8e1a0239" />

---
## Seleção de Elementos

```js
//Seleciona o elemento pela TAG e realiza a alteração interna.

let elemento =
  document.getElementById("C1");
elemento.innerHTML = "<p>XPTO</p>";
```
Principais Métodos de Seleção:

- **getElementsByTagName**: Seleciona os elementos pela **TAG**
- **getElementsByClassName**: Seleciona os elementos pela **CLASSE**
- **getElementsById**: Seleciona os elementos pela **ID**
- **getElementsByName**: Seleciona os elementos pelo **NOME**

## Funções em JavaScript

```js
//Formato tradicional (antigo)
function exibirSoma(a,b) {
  let c = a + b;
  alert('A soma será ${c}');
}
```
```js
// Arrow function (novo)
const exibirSoma = (a,b) => {
   let c = a + b;
  alert('A soma será ${c}');
}
```

## Eventos do **HTML**

Interatividade no HTML:
- Componentes de entrada e caixas de diálogo
- Utilização de eventos
- Resposta aos eventos através de funções JavaScript
- Possibilidade de associação dinâmia como ocorre no JQuery

---

Alguns Eventos do HTML
- onLoad
- onClick
- onDblClick
- onSubmit
- onChange
- onBlur
- onFocus
- onKeyPress
- onMouseOver
- onMouseOut

```js

// Exemplo: Mostra algo ao clicar

$("#cmd1").on("click", (event)=> {
  hiddenBox.show()
});
```
