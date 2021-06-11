# Copiar arquivos entre containers

Para copiar arquivo de um container em utilização para um determinado diretório.

```unix
    docker cp <nome_container>:/src/app.js ./copia/
```

Onde <nome_container>:/src/app.js é um arquivo de um diretório que está rodando e ./copia/ é uma pasta no atual diretorio