# FROM, ADD, RUN, COPY geram uma nova camada na imagem final
FROM ubuntu:18.04

# defini o diretorio para as linhas a partir daqui, os comandos vao ser setado no local x
# se voce mencionar um diretorio que nao existe dentro da imagem, ele ira ser criado
WORKDIR /copy

# puxa o arquivo do nosso host para dentro da imagem
# entao nesse exemplo a baixo, estou setando o workdir no /copy e puxando o txt para dentro da imagem
COPY host-file.txt .

WORKDIR /add

# copia o arquivo de uma url para nossa imagem
# ou puxar um arquivo compactado (TAR) para dentro da nossa imagem e descompacta
# mas qual a diferença entre ADD e COPY ? o add como tem varias funcionalidades a mais, ele é para casos mais complexos
# usar add somente quando copy nao serve
ADD add-files.tar.gz .
ADD https://www.docker.com/app/uploads/2023/08/logo-guide-logos-1.svg .

# usamos para correr comandos dentro da imagem, comandos bash como se fosse um terminal
RUN apt-get update && apt-get install -y \
    net-tools \ 
    curl \
    nginx \
    && rm -rf /var/lib/apt/lists/*