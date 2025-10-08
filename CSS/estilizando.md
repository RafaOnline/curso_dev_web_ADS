## CSS

A CSS é uma linguagem de estilo que fornece total controle sobre a apresentação de um documento escrito em HTML. Com ela, é possível alterar, entre outras coisas, a forma e o posicionamento dos elementos, as cores, os tipos e tamanhos de fontes.

## Seletore class e id:

O seletor de classe é definido a partir da declaração do atributo class em um elemento HTML. Já o seletor de identificação é definido com o atributo id.

Embora não exista um padrão ou preferência para utilização do seletor id ou class, é importante frisar que um id deve ser aplicado a **apenas um elemento**, enquanto a class pode ser aplicada a um ou **vários elementos**.

## CSS e HTML

Há três formas usuais de aplicar estilos em um documento HTML usando CSS: **Inline**, **Interna** e **Externa**. Além dessas, a HTML5 permite a aplicação em escopo.

## CSS inline

Essa forma envolve a declaração do estilo CSS diretamente na tag, no código HTML. A declaração inline faz uso do atributo style procedido por declarações separadas por ponto e vírgula “;”. Esse atributo pode ser usado em qualquer tag HTML.
       
    <p style="background-color: blue">Texto paragáfo</p>

## CSS interna

Também chamada de CSS incorporada, é declarada na seção <head> do documento HTML.

    <html>
      <head>
        <style type"text/css">
            p {
                background-color; blue;
            }
        </style>
      </head>
    </html>

## CSS externa

Nesse caso, os estilos são declarados em um arquivo externo, com extensão “.css” e vinculados ao documento HTML por meio da tag **<link>**.

    <html>
      <link rel="stylesheet" type="text/css" href="style.css">
    </html>
