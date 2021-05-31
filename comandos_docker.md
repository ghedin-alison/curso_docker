# Lista de comandos úteis do docker

#### Descrição dos containers em execução
``` unix
    docker ps
    docker container ls
```
---
#### Descrição dos containers já executados e em execução
``` unix
    docker container ls -a
```
---

#### Versão do docker
``` unix
    docker --version
```
---

#### Baixar imagem e rodar container
``` unix
    docker run <imagem>
```
---
 
## Container
 - Container é o docker rodando alguma imagem. 
 - Containers utilizam imagens para execução. Essas imagens possuem um dockerfile com instruções do que o container vai rodar pra poder executar.
 - Multiplos container podem ser executados em conjunto.
  - Fluxo é a partir de uma imagem programada, a executamos por meio de um container.
---

#### Baixar imagem
``` unix
    docker pull <imagem>
```
---

#### Executar de maneira interativa um container
``` unix
    docker run -it <imagem>
```
---

#### Executar container em background
##### detached -d
``` unix
    docker run -d <imagem>
```
---

#### Parar um container
``` unix
    docker stop <container name>
    docker stop <container id>

```
---
#### Reiniciar um container
``` unix
    docker start <container name>
    docker start <container id[:3]>

```
---
#### Definir nome de um container
##### flag --name
``` unix
    docker run --name <nome> <nome da imagem>
```
---

#### Expor portas flag -p 8080:80(porta que queremos acessar: porta do container)
##### -p portas
``` unix
    docker run -d -p 8080:80 nginx
```
---
#### Verificar log
``` unix
    docker logs <id ou nome>
```
---

#### Removendo um docker
``` unix
    docker -rm <id ou nome>
```
Se estiver em execução utilizar a flag -f para forçar

---