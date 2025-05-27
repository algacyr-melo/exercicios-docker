# ex04

## Quebrando o problema

1. Suba um container do MySQL (pode usar a imagem mysql:5.7),
utilizando um volume nomeado para guardar os dados.
    ```bash
    docker run --name ex04-docker -e MYSQL_ROOT_PASSWORD=my-secret-pw -v ex04-vol:/var/lib/mysql -d mysql:5.7
    ```

2. Crie um banco de dados
    ```bash
    docker exec -it ex04-docker mysql -u root -p
    ```
    ```sql
    CREATE DATABASE ex04_db;
    ```
    ![show-databases](./screenshots/show-dbs.png)

3. Pare o container
    ```bash
    docker stop ex04-docker
    ```

4. Suba novamente e verifique se os dados persistem
    ```bash
    docker start ex04-docker
    ```
    ```sql
    SHOW DATABASES;
    ```
    ![show-databases](./screenshots/show-dbs.png)
