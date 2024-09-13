```*FROM node:alpine*```
---
Especifica a imagem base que será utilizada para construir a imagem Docker.
Neste caso, é a imagem ```node:alpine```, que é uma versão mínima (baseada no Alpine Linux) do Node.js, contendo apenas o essencial para rodar uma aplicação Node.js, resultando em uma imagem mais leve.

```*COPY . /app*```
---
Copia todos os arquivos e diretórios do diretório atual (onde o Dockerfile está) para o diretório ```/app``` dentro do container. Isso inclui os arquivos de código da aplicação, como ```app.js``` e outros recursos necessários.

```*WORKDIR /app*```
---
Define o diretório de trabalho dentro do container como ```/app```. Isso significa que todos os comandos subsequentes executados dentro do container acontecerão dentro desse diretório.

```*CMD node app.js*```
---
Especifica o comando que será executado quando o container for iniciado.
Neste caso, está rodando o comando ```node app.js```, que inicia a aplicação Node.js contida no arquivo ```app.js```.