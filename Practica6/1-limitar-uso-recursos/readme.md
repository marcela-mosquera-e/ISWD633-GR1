# Limitar uso de memoria y procesador
Para crear y ejecutar los contenedores usar la imagen de nginx:alpine

### Memoria
Limitar la memoria RAM que el contenedor puede utilizar a 10 megabytes
```
docker run -d --name server-nginx --memory=10m nginx:alpine
```

Limitar la memoria RAM que el contenedor puede utilizar a 300 megabytes además el límite total de memoria y memoria swap combinados que el contenedor puede utilizar que sea 1 gigabyte
```
docker run -d --name server-nginx --memory=300m --memory-swap=1g nginx:alpine

```
**¿Cuántos megabytes de memoria swap puede utilizar el contenedor creado anteriormente?**


### Procesador
**¿Como saber el numero de procesadores virtuales que tiene una máquina?**

Limitar el uso de CPU a 1.5 núcleos
```
docker run -d --name server-nginx --cpus="1.5" nginx:alpine

```

Restringir el contenedor para que use los núcleos de CPU 0 a 2:
```
docker run -d --name server-nginx --cpuset-cpus="0-2" nginx:alpine

```

Restringir el contenedor para que use los núcleos de CPU 1 y 3:
```
docker run -d --name server-nginx --cpuset-cpus="1,3" nginx:alpine

```