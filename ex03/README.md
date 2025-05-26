# ex03

## Quebrando o problema

1. Inicie um container da imagem ubuntu com um terminal interativo
    ```bash
    docker run --rm -it ubuntu:24.04 bash
    ```
    ![1-run](screenshots/1-run.png)

2. Navegue pelo sistema de arquivos e instale o pacote curl utilizando apt
    ```bash
    apt update && apt install curl -y
    ```
    ![2-install-curl](screenshots/2-install-curl.png)
