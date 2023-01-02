# Indice

- [Dockers](#dockers)

# Install

Vamos a tener Docker y Docker compose
https://docs.docker.com/engine/install/ubuntu/

# Dockers

## commands

### run

```sh
# Toma el hello-world de las imagenes de docker y lo ejecuta en un contenedor
docker run <image name>
docker run hello-world

# !command reemplaza al startup command que se ejecuta por defecto,
# esto es una vez que el conteiner es creado, no se puede volver a reemplazar una vez que ya se genero
docker run <image name> <!command>
docker run busybox echo hi there

```

Usar docker run es igual a usar:

```sh
docker run = docker create + docker start

# docker create -> crea el contenedor
docker create <image name>

# docker start -> ejecuta el contenedor
docker start <container id>
```

### ps

Enlista todo los contenedores que estan siendo ejecutando

```sh

# Estan corriendo
docker ps

# Todos
docker ps -a

```

### restart

```sh

```

# Docker Compose
