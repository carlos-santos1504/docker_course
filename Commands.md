IMAGE
---
*[Construir o Docker]*: ```docker build -t app .```

*[Rodar a aplicação]*: ```docker run -it app sh  ```

*[Construir uma imagem app]*: ```docker build -t app .  ```

*[Executar o app na porta 3000]*: ```docker run -dp 127.0.0.1:3000:3000 app  ```

*[Criar versionamento da imagem utilizando TAG]*: ```docker build -t app:v1.0.0 .  ```

*[Remover uma imagem do docker]*: ```docker image remove app:v1.0.0  ```

*[Copiar um docker image]*: ```docker image tag app:latest app:v1.0.0  ```

*[Construir uma imagem do ID 7b8ff96f3057 com o nome do repositório com a tag v1]*: ```docker image tag 7b8ff96f3057 carlossantos1504/app:v1  ```

*[Criar uma imagem .tar]*: ```docker image save -o appv1.tar app:v1  ```

*[Criar a imagem a partir do .tar]*: ```docker image load -i appv1.tar ```


CONTAINERS
---
*[Visualizar os containers funcionando]*: ```docker ps  ```

*[Executar um container em background]*: ```docker run -d app:v2  ```

*[Executar o container nomeando-o para manga]*: ```docker run -d --name manga app:v2  ```

*[Visualizar opções de logs]*: ```docker logs --help  ```

*[Executar um container (banana) em background (-d) publicando (-p) na porta (3000) para o host (80)]*: ```docker run -d -p 80:3000 --name banana app:v2  ```

*[Visualizar os arquivos do container banana]*: ```docker exec banana ls  ```

*[Iniciar/parar container]*: ```docker start/stop banana  ```

*[Remover de forma forçada o container]*: ```docker rm -f banana  ```


VOLUMES
---
*[Criar um volume]*: ```docker volume create app-dados  ```

*[Visualizar os conteúdos do volume]*: ```docker volume inspect app-dados  ```

*[Executar associando o volume app-dados]*: ```docker run -d -p 80:3000 --name kiwi -v app-dados:/app/dados app:v2  ```

*[Acessar a imagem]*: ```docker exec -it kiwi sh  ```

*[Copiar arquivo do container kiwi2 para a pasta da aplicação]*: ```docker cp kiwi2:/app/teste.txt .  ```

*[Copiar um arquivo txt da aplicação para um container]*: ```docker cp README.txt kiwi2:/app```


LIMPEZA DO DOCKER
---
*[Parar todos os containers em execução (opcional)]*: ```docker stop $(docker ps -aq)```

*[Remover todos os containers]*: ```docker rm $(docker ps -aq)```  

*[Remover todas as imagens]*: ```docker rmi $(docker images -q) ```  

*[Remover todos os volumes]*: ```docker volume rm $(docker volume ls -q) ```  

*[Remover todas as redes]*: ```docker network prune ```  
