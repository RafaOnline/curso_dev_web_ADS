# Frameworks em CSS
Abaixo possui algun frameworks que podem ajudar em desenvolvimentos front-end
- Foundation: https://get.foundation/
- Semantic UI: https://semantic-ui.com/
- Bootstrap: https://getbootstrap.com/

## Prática
Aplicando o sistema de grid do Bootstrap

Código:


```html

    <!DOCTYPE html>
    <html lang="pt-BR">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Grid em bootstrap</title>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-                  sRIl4kxILFvY47J16cr9ZwB07vP4J8+LH7qKQnuqkuIAvNWLzeN8tE5YBujZqJLB" crossorigin="anonymous">
      <style type="text/css">
          div{
                padding: 5px;
                color: #fff;
                font-weight: bold;
            }

          .border{
              border: 1px solid #999999;
          }
  
          .container{
              background: green;
              margin-bottom: 100px;
          }
  
          .container-fluid{
              background: orange;
          }
    </style>
    </head>
      <body>
        <h1 class="text-center">Container: largura definida e responsiva</h1>

        <div class="container text-center">

        <div class="row">
            <div class="col border">
                Linha 1 - Coluna 1
            </div>

            <div class="col border">
                Linha 1 - Coluna 2
            </div>
        </div>

        <div class="row">
            <div class="col border">
                Linha 2 - Coluna 1
            </div>

            <div class="col border">
                Linha 2 - Coluna 2
            </div>

            <div class="col border">
                Linha 2 - Coluna 3
            </div>
        </div>

        </div>
        
          <h1 class="text-center">Container-Fluid: Largura 100%</h1>
          <div class="container-fluid">

          <div class="row">
              <div class="col-4 border">
                  Linha 1 - Coluna 1
              </div>
  
              <div class="col-8 border">
                  Linha 1 - Coluna 2
              </div>
          </div>

          <div class="row">
              <div class="col-6 border">
                  Linha 2 - Coluna 1
              </div>
  
              <div class="col-3 border">
                  Linha 2 - Coluna 2
              </div>
  
              <div class="col-3 border">
                  Linha 2 - Coluna 3
              </div>
          </div>
    </body>
    </html>
```
Resultado


<img  width="679" height="360" alt="image" src="https://github.com/user-attachments/assets/45137286-10c3-431a-8b5b-55d2c869c002" />
