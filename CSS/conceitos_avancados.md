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









