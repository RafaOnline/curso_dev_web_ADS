# Conceitos avançados em CSS

## Pseudo-elementos:
São palavras-chaves que podem ser adicionadas ou relacionadas a um seletor para estilizar uma parte específica dele.

Exemplo: 

<img width="307" height="113" alt="image" src="https://github.com/user-attachments/assets/752c2cb8-72af-401e-8bb5-08fae0da7339" />

Resultado:

<img width="371" height="118" alt="image" src="https://github.com/user-attachments/assets/aa2c964b-34de-4db5-af59-7983442a6eb2" />



## Pseudo-classes:
São utilizados para definir um estado especial de um elemento.


Exemplo:

<img width="269" height="83" alt="image" src="https://github.com/user-attachments/assets/db2bc635-9af0-41f8-bb08-e9e3370c795b" />

Resultado:

<img width="222" height="86" alt="image" src="https://github.com/user-attachments/assets/370a1e1f-7efa-43fb-96d0-32fd7fa5002c" /> ---->
<img width="212" height="86" alt="image" src="https://github.com/user-attachments/assets/d09d605a-df3e-4b85-b3a5-bdb433ff1c5e" />

## Box model:
Está relacionado ao conceito de como é feioto o desing e layout em CSS.


Os boxes, possuem quatro componentes principais:
- Margem(margin)
- Borda(border)
- Preenchimento(padding)
- Conteúdo(content)

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/69ba2ba4-8de9-4245-9c6f-f2dc034ed507" />


## Grid layout x Flexbox layout
São dois conceitos de estrutura visuais de páginas

**Grid layout:**
Elementos em colunas ou linhas podendo trabalhar com os dois juntos


**Flex layout:**
Elementos que ficam somente em coluna ou linha somente um tipo de layout.


<img width="311" height="236" alt="image" src="https://github.com/user-attachments/assets/bc4c91cd-d7c0-4302-85a0-4d8d8ba1e1aa" />


## Posicionamento de elementos
Elementos podem ser posicionados de várias maneiras.

**Flexbox Row** (display: flex; flex-direction: row;)

- Organiza os elementos horizontalmente (em linha).
- Os itens são colocados lado a lado, da esquerda para a direita.
- Ideal para menus, barras de navegação, ou qualquer layout horizontal.


**Flexbox Col** (display: flex; flex-direction: column;)

- Organiza os elementos verticalmente (em coluna).
- Os itens são empilhados de cima para baixo.
- Útil para listas, colunas de conteúdo, etc.


**Grid** (display: grid;)

- Permite criar layouts bidimensionais (linhas e colunas).
- Muito poderoso para layouts complexos.
- Exemplo: grid-template-columns: 1fr 2fr; define duas colunas com larguras proporcionais.


**Posição Absoluta** (position: absolute;)

- O elemento é removido do fluxo normal do documento.
- Posicionado em relação ao elemento pai com position: relative.
- Exemplo: top: 10px; left: 20px; posiciona o elemento 10px do topo e 20px da esquerda do pai.


**Posição Estática** (position: static;)

- É o comportamento padrão.
- O elemento segue o fluxo normal do documento.
- Não responde a propriedades como top, left, etc.


**Posição Relativa**(position: relative;)

- O elemento permanece no fluxo normal, mas pode ser ajustado com top, left, etc.
- Serve também como referência para elementos com position: absolute.


**Posição Fixa** (position: fixed;)

- O elemento é fixado em relação à janela de visualização (viewport).
- Não se move ao rolar a página.
- Exemplo: position: fixed; bottom: 0; fixa o elemento no rodapé da tela.

# Exemplo em **html**

```html
    <!DOCTYPE html>
    <html lang="en">

    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Posicionamento em CSS</title>
    <style>


          #container-flexbox-row{
              display: flex;
              flex-direction: row;
              background-color: green;
          }
  
          #container-flexbox-col {
              display: flex;
              flex-direction: column;
               background-color: green;
  
          }
  
          #container-grid{
              display: grid;
              grid-template-columns:
                  50px 50px 50px 50px 50px;
             /* grid-template-row:
                  50px 50px 50px 50px 50px*/
          }
  
          #container-grid div {
              border: 1px solid black;
              background: red;
          }
  
          #container-absolute {
              background-color: orange;
              position: absolute;
              top: 80px;
              right: 0;
              height: 100px;
              width: 200px;
              border: 3px solid black;
              color: #000;
          }
  
          #container-static {
              border: 3px solid #73AD21;
              width: 300px;
              background: rgb(106, 90, 205);
          }
  
          #container-relative{
              position: relative;
              left: 30px;
              border: 3px solid green;
              width: 300px;
              background:rgb(106, 90, 205);
          }
  
          #container-fixed {
              position: fixed;
              bottom: 0;
              right: 0;
              width: 300px;
              background-color: orange;
              border: 3px solid black;
          }
      </style>
    </head>

    <body>
  
      <h1>Flexbox row</h1>
      <div id="container-flexbox-row">
          <div>
              Flexbox 1
          </div>
  
          <div>
              Flexbox 2
          </div>
  
          <div>
              Flexbox 3
          </div>
      </div>
  
      <h1>Flexbox col</h1>
      <div id="container-flexbox-col" >
          <div>
              Flexbox 1
          </div>
  
          <div>
              Flexbox 2
          </div>
  
          <div>
              Flexbox 3
          </div>
      </div>
  
      <h1>Grid</h1>
      <div id="container-grid">
          <div>col1</div>
          <div>col2</div>
          <div>col3</div>
          <div>col4</div>
          <div>col5</div>
      </div>
  
      <h1>Posição absoluta</h1>
      <div id="container-absolute">
          <div>
              Absolute: posicionado em relação ao elemento
              anterior ou, na ausência desse, em relação á tag body.
          </div>
      </div>
  
      <h1>Posição estática</h1>
      <div id="container-static">  
          <div>
              Static: Posicionamento natural do elementos.
          </div>
      </div>
  
      <h1>Posição relativa</h1>
      <div id="container-relative">
          <div>
              Relative: posicionado em a relação á sua posição natural(static)
          </div>
      </div>
  
      <h1>Posição fixa</h1>
      <div id="container-fixed">
          <div>
              Fixed: posicionado de forma fixa em relação ao viewport.
          </div>
      </div>
    </body>

    </html>
```

Resultado:

<img width="1342" height="592" alt="image" src="https://github.com/user-attachments/assets/390448e2-7449-4d8b-90a6-300db4ad862e" />








