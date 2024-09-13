O arquivo ```docker-compose.yml``` define a configuração de uma aplicação composta por três serviços:

Backend:
---
Um serviço de backend que será construído a partir do diretório ```./backend```, exposto na porta 5000, e depende do Redis.

Frontend:
---
Um serviço de frontend que será construído a partir do diretório ```./frontend```, exposto na porta 80.

Redis: Um serviço de cache Redis utilizando a imagem ```redis:alpine```.
---
Todos os serviços estão conectados a uma rede interna chamada ```app-network```, que permite a comunicação entre eles.