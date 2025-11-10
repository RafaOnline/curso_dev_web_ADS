# Laços: Estruturas de repetição

### Caracteristicas 
- Também são amplamente usadas;
- Independe do paradigma de programação;
- Proporciona a redução de linhas de código;
- PHP suporta diferentes estruturas de repetição: whle, do-while e foreach;
- Cada estrutura tem suas particularidades;
- POdem ser usadas várias vezes no memso programa;


<img width="310" height="316" alt="image" src="https://github.com/user-attachments/assets/1eff7323-989c-4f8e-999a-dba616606683" />

- As estruturas de repetição possibilitam executar um bloco de código múltiplas vezes;
- Automatizar tarefas repetitivas;
- Iterar sobre conjunto de dados;
- Deve-se atentar para a condição, de modo que não entre em loop infinito;

# Laços: Estruturas de Decisão

### Caracteristicas 
- Precisamnos repetirar a verificação se a idade é maior ou igual a 12?
- E se a idade for maior que 18?

<img width="310" height="316" alt="image" src="https://github.com/user-attachments/assets/7c65cf32-60ed-4a99-995b-4005b88fdfa9" />

- É comum utilizar estruturas condicionais em programas;
- Proporciona maior flexibilidade;
- O programa pode seguir caminhos distintos, dependendo das condições estabelecidades;
- Pode- ser utilizar estruturas condicionais várias vezes no msmo programa;
- É comumm utilizar operadores no estabelecimento das condições;
- Os programas ser compostos por um encadeamento de estruturas condicionais e de repetição;

## Prática

**Contextualização**

- Considere ma turma com dez alunos;
- As notas de uma determinada prova já foi lançadas;
- Para simplificar, vamos considerar que estar notas estejam em um array;
- O sistema deve calcular a média da turma e, depois, exibir uma mensagem de acordo com o resultado da média;
- A aplicação do servidor que realiza estas ações é desenvolvida em PHP;

**Código**
```html
  <!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Prática PHP</title>
</head>
<body>

    <?php 
        // Cria um array com 10 notas de alunos
        $notas = [6.6, 8.5, 9.2, 7.8, 6.1, 7.9, 8.3, 7.7, 6.4, 8.6];

        // Inicializa a variável $soma com zero para evitar erro de variável indefinida
        $soma = 0;

        // Percorre o array de notas somando cada valor à variável $soma
        foreach ($notas as $i) {
            $soma += $i;
        }

        // Calcula a média dividindo a soma pelo número total de notas
        $media = $soma / 10;

        // Verifica se a média é menor que 6.0 e exibe mensagem correspondente
        if ($media < 6.0) {
            echo "Média da turma = " . $media . ". Estude mais!";
        }

        // Verifica se a média é exatamente 6.0 e exibe mensagem correspondente
        elseif ($media == 6){
            echo "Média da turma = " . $media . ". Na média!";
        }

        // Se a média for maior que 6.0, exibe mensagem de desempenho acima da média
        else {
            echo "Média da turma = " . $media . ". Acima de média!";
        }
    ?>

</body>
</html>
```

**Resultado**


<img width="600" height="70" alt="image" src="https://github.com/user-attachments/assets/c533c99a-17b6-4c75-8192-b78f07252e12" />

