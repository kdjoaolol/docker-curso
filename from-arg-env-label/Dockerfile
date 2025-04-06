ARG TAG=latest

# imagem base
# FROM alpine:3.16.2  OU 
FROM alpine:$TAG

# variaveis presentes apenas durante o build, podemos definir valor default ou passamos quando colocar o docker build 
# ARG CONTAINER_NAME OU colocando o = (que é o default)
ARG CONTAINER_NAME_ARG=Container-A

# cria uma variavel de ambiente e ficará presente na imagem final, diferente do ARG e nao pode ser configurado no momento do build
# usamos o -> {x:-y} para definir um valor default
# ENV CONTAINER_NAME_ENV=$CONTAINER_NAME_ARG
# se quisessemos colocar espaço, colocamos entre aspas duplas ${CONTAINER_NAME_ARG:-"Container A"}
ENV CONTAINER_NAME_ENV=${CONTAINER_NAME_ARG:-"Container A"}

# documentação  de codigo
LABEL maintainer="Jv"