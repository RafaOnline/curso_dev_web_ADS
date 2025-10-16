# Conceitos e sintaxe do JavaScript

## Árvore DOM(document object model)
Interpretação das **TAGS** de forma **Hierárquica**

<img width="500" height="783" alt="image" src="https://github.com/user-attachments/assets/a745f4a1-95d9-43c4-98e3-46ca8e1a0239" />

---
## Seleção de Elementos

```js
let elemento =
  document.getElementById("C1");
elemento.innerHTML = "<p>XPTO</p>";
//Seleciona o elemento pela TAG e realiza a alteração interna.
```
Principais Métodos de Seleção:

- **getElementsByTagName**: Seleciona os elementos pela **TAG**
- **getElementsByClassName**: Seleciona os elementos pela **CLASSE**
- **getElementsById**: Seleciona os elementos pela **ID**
- **getElementsByName**: Seleciona os elementos pelo **NOME**
