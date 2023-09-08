# nginx
docker build -t alanjunqueira/nginx-with-vim:latest . (Cria a imagem)
docker run -it alanjunqueira/nginx-with-vim bash (Starta e entra na imagem)

# ubuntu
docker build -t alanjunqueira/ubuntu-hello:latest . (Cria a imagem)
docker build -t alanjunqueira/nginx:prod . -f Dockerfile.prod  --> Executa na pasta atual

### Extra
docker run --rm "nome da imagem" --> Deleta após executar.
docker rm $(docker ps -a -q) -f --> Mata todos os containers

# Network
docker network prune --> Remove all unused networks

## Laravel
docker run --rm -d --name laravel -p 8000:8000 alanjunqueira/laravel
Opcional: --> --host=0.0.0.0 --port=8001

## Escolher o Dockerfile de prod
docker build -t alanjunqueira/hello-express . -f Dockerfile.prod