# Manipulação com Vetores

### Acesso e Alteração de Valores

**Bubble Sort** :
Esse código implementa o Bubble Sort, um algoritmo simples de ordenação. Ele compara pares de elementos adjacentes e os 
troca de lugar se estiverem fora de ordem, repetindo esse processo até que o vetor esteja completamente ordenado.
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>

<body>

    <script>
        // Função de ordenação usando o algoritmo Bubble Sort
        const bubble = (v) => {
            let ordenado = false; // Flag para verificar se o vetor está ordenado

            // Enquanto o vetor não estiver ordenado
            while (!ordenado) {
                ordenado = true; // Assume que está ordenado

                // Percorre o vetor do segundo elemento até o final
                for (let i = 1; i < v.length; i++) {
                    // Se o elemento anterior for maior que o atual, troca os dois
                    if (v[i - 1] > v[i]) {
                        const aux = v[i];           // Guarda o valor atual
                        v[i] = v[i - 1];            // Move o valor anterior para a posição atual
                        v[i - 1] = aux;             // Coloca o valor atual na posição anterior
                        ordenado = false;           // Marca como não ordenado para continuar o loop
                    }
                }
            }
        }

        // Vetor de valores a ser ordenado
        const valores = [3, 1, 7, 6, 4];

        // Exibe o vetor original no console
        console.log(valores);

        // Chama a função de ordenação
        bubble(valores);

        // Exibe o vetor ordenado no console
        console.log(valores);
    </script>

</body>

</html>
```

Resultado:

<img width="551" height="54" alt="image" src="https://github.com/user-attachments/assets/7bc1bad3-ee7f-4dee-896a-1e1f83e1c566" />
