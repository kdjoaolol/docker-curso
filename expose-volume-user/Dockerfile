# RESUMO DO DOCKER
# USER a gente defini um usuario na imagem, usuario root para operar a imagem
# precisamos criar esse codigo grande no run para configurar o nginx 
# e dar permissão para o usuario criado
# o EXPOSE serve pra expor uma porta do container para o host
# o VOLUME serve para setar um diretorio em que sera criado o volume na imagem

FROM nginx:1.23.3-alpine

COPY default.conf /etc/nginx/conf.d/default.conf 
COPY nginx.conf /etc/nginx/nginx.conf

RUN addgroup -g 1000 -S jv \
    && adduser -S -D -H -u 1000 -h /var/cache/nginx -s /sbin/nologin -G jv -g jv jv \
    && chown -R jv:jv /var/cache/nginx \
    && chown -R jv:jv /var/log/nginx \
    && chown -R jv:jv /etc/nginx/conf.d \
    && touch /var/run/nginx.pid \
    && chown -R jv:jv /var/run/nginx.pid

# cria um usuario no meu container, usuario:grupo ou usando o id_usuario:grupo_usuario
USER jv

# expoe uma porta da imagem
EXPOSE 8010 

# docker vai criar e reservar um volume pra cada vez que rodamos o container
# vou pegar a pasta a baixo e colocar na minha maquina host 
VOLUME /usr/share/nginx/html