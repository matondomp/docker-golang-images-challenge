# docker-golang-images-challenge
Golang challeng docker images

Passo 1:
  docker pull freitaspedros/fullcycle
Passo 2: 
   docker run -d --name [container_name] -p 3500:10000 freitaspedros/fullcycle
Passo 3:
  Vai no browser digite: http://localhost:3500/

OU ainda criar uma imagem com o seguinte comando:
  Passo 1: 
    docker-compose up -d 
  Passo 2:
    http://localhost:10000/
