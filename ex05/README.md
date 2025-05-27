# ex05

## Quebrando o problema

1. Crie um container com a imagem alpine passando uma variável
de ambiente chamada MEU_NOME com seu nome.
    ```bash
    docker run -e MEU_NOME=algacyr alpine:3.21.3
    ```

2. Execute o container e imprima o valor da variável
com o comando echo.
    ```bash
    docker run -e MEU_NOME=algacyr alpine:3.21.3 sh -c 'echo "$MEU_NOME"'
    ```
