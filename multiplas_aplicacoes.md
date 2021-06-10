# Execução de múltiplas aplicações

Podemos inicializar vários containers com a mesma imagem

No terminal:
### Criar uma imagem de nome node3000
``` unix
    docker run -d -p 3000:3000 --name node3000 <imagem>
```


### Criar uma imagem de nome node4000
``` unix
    docker run -d -p 4000:3000 --name node4000 <imagem>
```

### Criar uma imagem de nome node5000
``` unix
    docker run -d -p 5000:3000 --name node5000 <imagem>
```

Com isso temos 3 aplicações funcionando em paralelo utilizando a mesma imagem do node.