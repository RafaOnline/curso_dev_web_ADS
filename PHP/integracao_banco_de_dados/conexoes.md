# Conexões persistentes

**Características**

*   É importante liberar recursos que não são mais utilizados nos programas, como espaços de memória de variáveis, conexões com bancos de dados;
*   Ou seja, se não estiver usando o banco de dados, encerre a conexão;
*   Porém, se o mesmo usuário desejar realizar outras consultas ao banco, pode ser interessante manter a conexão ativa;
*   PHP oferece recursos para conexões persistentes;

**Conclusão**

*   Conexões persistentes com bancos de dados em PHP são uma técnica para manter uma conexão aberta ao banco de dados entre diferentes solicitações feitas ao servidor web;
*   Em vez de estabelecer uma nova conexão a cada vez que um script PHP é executado, uma conexão persistente reutiliza uma conexão existente;
*   Esta abordagem pode melhorar o desempenho de aplicações que fazem uso intensivo de bancos de dados.



