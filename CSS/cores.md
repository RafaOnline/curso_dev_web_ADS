# Formas de escrita de cores

As cores em CSS pode ser escritas de três modos:

- Com palavras chaves usando os nomes das cores.
- Com um sistema de coordenadas RGB, rgb() ou rgba().
- Com um sistema de coordenada cilíndrica HSL, com anotações hsl() hsla().

Exemplo:
      
    <!DOCTYPE html>
    <html lang="en">

    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Teste de cores</title>
    <style>
        #rgb {
            background-color: rgb(255,0,51);
        }

        #rgba {
            background-color: rgba(255,0,51,40%);
        }

        #hsl {
            background-color: hsl(0, 100% , 50%);
        }

        #hsla {
            background-color: hsla(0,100%,50%,40%);
        }
    </style>
    </head>

    <body>
        <div>
          <div id="rgb">
              RGB - Red, Green, Blue
          </div>
  
          <div id="rgba">
              RGBA
          </div>
  
          <div id="hsl">
              HSL - Hue, Saturation, Lightness
          </div>
  
          <div id="hsla">
              HSLA
          </div>
        </div>
    </body>

    </html>

Resultado:

<img width="243" height="93" alt="image" src="https://github.com/user-attachments/assets/169186f9-c3a6-4cb5-9d3a-05bfac4960ca" />
