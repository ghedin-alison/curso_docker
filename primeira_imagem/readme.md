# Ordem de execução do projeto

1 - Baixado o npm pra trabalhar com o Node
2 - comando 
```unix
    npm init -y
```
Comando pra iniciar um projeto de node, isso cria o package.json onde podemos instalar nossas dependencias

3 - comando 
```unix
    npm install express
```
Instala o framework express pra poder acessar essa aplicação no navegador

4 - cria o app.js com configurações do express e mensagens para garantir que a imagem está sendo executada corretamente

5 - comando 
```unix
    node app.js
```

6 - Cada linha do dockerfile cria uma camada dentro do docker.
FROM node => copia da imagem base do node
WORKDIR /app => diretorio de execução da aplicacao
COPY package*.json . => copia esses arquivos pra dentro do diretorio /app
RUN npm install => comando pra executar o npm install no container
COPY . . => copia tudo que está nessa pasta pra dentro do container
EXPOSE 3000 => porta exposta
CMD ["node", "app.js"] => linha de comando executada para iniciar a aplicação

7 - dentro do diretório onde está a imagem, executar 
```unix
    docker build <diretorio da imagem>
    ou
    docker build .
```

8 - executar
```unix
    docker run <imagem>
```
Para esse caso é ideal já rodar o caomando expondo a porta configurada no dockerfile, no caso, 3000
```unix
    docker run -d -p 3000:3000 49204118949a
```    