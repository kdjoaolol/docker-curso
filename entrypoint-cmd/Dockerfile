FROM alpine:3.16.2

RUN apk add ansible

ENV ANSIBLE_HOST_KEY_CHECKING=False

ENTRYPOINT ["ansible"]

# se tiver espaço, usamos o , "" -> ["ansible", "--help"]
# geralmente quando fazemos o docker container run ... imagem:version [TUDO APOS VAI SUBSTITUIR O CMD e o ENTRPOINT PERMANECE]
CMD ["--help"]
