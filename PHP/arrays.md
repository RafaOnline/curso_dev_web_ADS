# Vetores e Funções

### Arrays: Vetores
**Características**
- Vetores são muito utilizados em programação;
- Possibilita armazenar múltiplos conteúdos em uma única variável;
- Possibilita a organnização e manipulação dos dados de forma simplificada;

  <img width="300" height="310" alt="image" src="https://github.com/user-attachments/assets/dd850ad0-9a92-4b3f-9ba6-cce8430145e8" />


  ### Demonstração de prática do uso de array multidimensional em PHP
  **Contextualização**
  - Considere a situação em que os alunos de uma turma fazem duas povas no sementre letivo, P1 e P2;
  - Ao lado dos nomes dos alunos, devem aparecer as notas de provas, conforme está mostrado a seguir;
    - João: P1: 8.7, P2: 9.4
    - Maria: P1: 9.2, P2: 8.9
    - Luís: P1: 7.8, P2: 8.4
    - Fernanda: P1: 8.7, P2: 9.1
  - Neste contexto, a utilização de array multidimensional é mais indicado para armazenar os nomes e notas dos alunos;

**Código**
```php
<?php
    // Criação de um array multidimensional com os dados dos alunos.
    // Cada sub-array contém: nome do aluno, nota da P1 e nota da P2.
    $alunos = array(
        array("João", 8.7, 9.0),
        array("Maria", 9.2, 8.9),
        array("Luis", 7.8, 8.4),
        array("Fernanda", 8.7, 9.1)
    );

    // Exibe os dados do primeiro aluno (João): nome, nota da P1 e nota da P2.
    echo $alunos[0][0] . ": P1:" . $alunos[0][1] . ": P2:" . $alunos[0][2] . "<br>";

    // Exibe os dados do segundo aluno (Maria).
    echo $alunos[1][0] . ": P1:" . $alunos[1][1] . ": P2:" . $alunos[1][2] . "<br>";

    // Exibe os dados do terceiro aluno (Luis).
    echo $alunos[2][0] . ": P1:" . $alunos[2][1] . ": P2:" . $alunos[2][2] . "<br>";

    // Exibe os dados do quarto aluno (Fernanda).
    echo $alunos[3][0] . ": P1:" . $alunos[3][1] . ": P2:" . $alunos[3][2] . "<br>";
?>
```

### 📌 Resumo da funcionalidade
Este script PHP cria uma lista de alunos com suas respectivas notas em duas provas (P1 e P2) e exibe essas informações formatadas na tela. Cada linha mostra o nome do aluno seguido das notas de cada prova.
