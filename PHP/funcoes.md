# Funções em PHP
**Características**

- Muito comum no desenvolvimento de software;
- Modularização: divisão de um problema maior e mais complexo em partes menores, denominadas Módulos, de mais fácil entendimento e implementação;
- PHP tem suas funções próprias;
- Podemos implementar nossas funções;
- Reaproveitamento.

**Conclusão**

- As funções em PHP são componentes essenciais para a criação de código limpo, modular e reutilizável;
- Elas ajudam a estruturar melhor o código, melhorar a legibilidade e facilitar a manutenção;
- Compreender as características das funções e como utilizá-las de forma eficaz é crucial para qualquer desenvolvedor, independentemente da linguagem de programação.

### Programando funções

**Contextualização**

*   Considere um array unidimensional, que contém o nome de um aluno, além das duas notas de provas;
*   Vamos implementar uma função que calcule a média das duas notas;
*   Depois, o programa deve exibir o nome do aluno e a sua média;
*   A título de exemplo, seja o array:

    João   8.8   9.4

*   A função calcula a média de 8.8 e 9.4;
*   Finalmente, o programa deve exibir a seguinte saída:

    João tem média igual a 9.1

Código:
```php
<?php

    //Implementação da função que calcula a média
    function calc_media($n1, $n2) {
        return ($n1 + $n2)/ 2;
    }

    // Definição do array que contém os dados do aluno
    $aluno = array("João", 8.8, 9.4);

    // Chamada da função que calcula a média
    $media = calc_media($aluno[1], $aluno[2]);

    //Imprimindo os dados na tela
    echo $aluno[0]." tem média igual a ". $media;

?>
```

**Conclusão**

*   Funções permitem modularizar o código, tornando-o mais organizado e fácil de manter;
*   Reutilização de código evita redundância e facilita a manutenção e atualização;
*   PHP oferece um vasto conjunto de funções internas para diversas tarefas;
*   Funções definidas pelo usuário podem ser criadas para atender necessidades específicas, complementando as funções internas;
*   Importante diferenciar a implementação da função e sua utilização;




