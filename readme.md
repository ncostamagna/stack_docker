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

# coloco un nombre a la imagen
docker run --name <container name> <image name>

# docker interactivo (it), corremos fedora y entramos a la terminal
# cuando hago exist el contenedor deja de correr
docker run -it fedora bash


# -d corre en background, tienen que ser imagenes que esten preparadas para trabajar en background
docker run -d nginx

# si ponemos en modo interactivo forzamos a que vaya en modo background
docker run -d -it fedora
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

#tiltramos por nombre
docker ps -a -f name=<container name>

```

### prune

Remueve todos los contenedores que estan parados, networks que no son usadas, limpia todo.<br />
Es recomendable usarlo para limpiar todo lo que no es utilizado, y no ocupar espacio alpedo

```sh
docker system prune
```

### logs

POdemos ver los logs de los contenedores

```sh
docker logs <container id>
```

### stop & kill

```sh

docker stop <container id>

# Bajalo si o si, y no hagas nada
docker kill <container id>
```

# Docker Compose
