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
