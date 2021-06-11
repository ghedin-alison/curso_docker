# incluir tag em imagens

### Para incluir tag em imagens com nome da imagem e nome da tag
``` unix
    docker tag 1053fe3ecb42 imagem_node:tag_node
```
### Para incluir nome e tag em imagens já no build para uma pasta onde já existe o Dockerfile
``` unix
    docker build -t node_src:ultima .
```
