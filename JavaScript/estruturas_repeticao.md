# Estruturas de repetição

## Comando `while` - Estrutura Enquanto/Faça

**Repetição Condicional com Teste no Início**
- Comandos são executados enquanto a condição for verdadeira
- Para mais de uma instrução, é obrigatório delimitar o bloco com chaves, mas para uma instrução simples as chaves são opcionais

```javascript
let a = 1;
while(a <= 10 ){
  console.log(a);
  a++;
}
```

## Comando `do while` - Estrutura Faça/Enquanto

**Repetição Condicional com Teste ao Final**
- Comandos são repetidos enquanto a condição for verdadeira, com teste ao final
- Para mais de uma instrução, é obrigatório delimitar o bloco com chaves, mas para uma instrução simples as chaves são opcionais

```javascript
let a = 1;
do {
  console.log(a);
  a++;
} while(a <= 10);
```

## Comando `for` - Estrutura Para/Faça
- Comandos são executados para cada valor fornecido na estrutura de controle
- Divide a estrutura em três áreas: Inicialização, teste e incremento

```javascript
for (let a =1; a <= 10; a++){
  console.log(a);
}
```

### Comando `for in` - Iteração em Objeto

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Estruturas de repetição</title>
</head>
<body>
    <h2>for in</h2>
    <p>Iteração nas propriedades de um objeto</p>
    <p id="d1"></p>
    <script>
        const person = {fname:"John", iname:"Doe", age:25};
        let text = "";
        for (let x in person){
            text += person[x] + " "; // x é o nome do campo
        }
        document.getElementById("d1").innerHTML = text;
    </script>
</body>
</html>
```

Resultado:

<img width="414" height="181" alt="image" src="https://github.com/user-attachments/assets/29bd8ab8-e1bc-426d-b7cc-d01ecdeeda08" />

### Comando `for in` - Iteração em Vetor (Posicional)

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Estruturas de repetição</title>
</head>
<body>
    <h2>for in</h2>
    <p>Iteração nas propriedades de um objeto</p>
    <p id="d1"></p>
    <script>
        const cars = ["BMW","Volvo","Saab", "Ford"];
        let text = "";
        for (let x in cars){
            text += cars[x] + " "; // x é o nome do campo
        }
        document.getElementById("d1").innerHTML = text;
    </script>
</body>
</html>
```

### Comando `for of` - Iteração em Vetor (Elemento)
Pega o elemento em si não sua posição

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Estruturas de repetição</title>
</head>
<body>
    <h2>for of</h2>
    <p>Iteração nas propriedades de um objeto</p>
    <p id="d1"></p>
    <script>
        const cars = ["BMW","Volvo","Saab", "Ford"];
        let text = "";
        for (let x of cars){
            text += x + " "; // x é o nome do campo
        }
        document.getElementById("d1").innerHTML = text;
    </script>
</body>
</html>
```
