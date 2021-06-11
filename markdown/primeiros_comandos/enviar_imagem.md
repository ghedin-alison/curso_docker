# Envio de imagens para o Docker Hub

A nomenclatura no diretorio tem que ter o mesmo nome que no docker hub. Normalmente criamos no hub e depois renomeamos no diretorio.

```unix
    docker build -t ghedin/<imagem>:tag .
```

```unix
    docker push ghedin/<imagem>:tag
```

Para enviar imagem é necessário estar autenticado

```unix
    docker pull ghedin/<imagem>:tag
```
Para baixar imagem


```unix
    docker push ghedin/<imagem>:tag
```
Para atualizar uma imagem, basta repetir o processo atualizando a tag