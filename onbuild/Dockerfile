# ONBUILD nao podemos usar FROM nem MAINTAINER
# ONBUILD basicamente pega o momento que usamos a imagem para criar um container que 
# ele puxa as informações

FROM nginx:1.23.3-alpine

ONBUILD WORKDIR /usr/share/nginx/html
ONBUILD COPY index.html . 
ONBUILD RUN date +"%T" >> index.html