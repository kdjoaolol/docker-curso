FROM nginx:1.23.0-alpine


# aqui setamos os parametros do meu healthcheck e no CMD a baixo, colocamos
# o que ele vai testar, nesse caso ele vai ver se o localhost esta rodando
HEALTHCHECK --interval=10s --timeout=5s --start-period=15s --retries=2 \ 
    CMD curl -f http://localhost/

# aqui setamos qual o sinal que o docker vai nos retornar
# tem uma lista com todos esses sinais
STOPSIGNAL SIGKILL