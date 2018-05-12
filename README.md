# Containers com Docker

Para instalar o docker, basta entrar no site oficial e selecionar escolher o sistema operacional que será utilizado e seguir o passo a passo.
https://docs.docker.com/install/

### Primeiro container

Para entender como funciona um container, vamos criar um de ngnix (Servidor Web). Antes precisamos baixar a imagem docker do container, basta executar o comando:
```bash
docker pull ngnix
````
Após a finalização do download da imagem, podemos executar a mesma utilizando o comando:
```bash
docker run -p 80:80 --name ngnix ngnix
```
O atributo **-p** serve para fazermos redirecionamento de portas, nesse caso estamos apontando a porta **80** do nosso host para a porta **80** do nosso container.

Para visualizar as informações do container basta rodar o comando:
```bash
docker container inspect ngnix
```

Para acessar o servidor web, abra um navegador no seu host e entre em **http://localhost** ou **http://ip do host**
