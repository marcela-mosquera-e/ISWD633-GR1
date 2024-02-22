# Healthcheck
Para crear y ejecutar los contenedores usar la imagen de nginx:alpine


### Crear un proceso que valide que el contenedor está funcionando

```
docker run -d --name server-nginx --health-cmd="curl http://localhost" --health-interval=3s --health-start-period=5s --health-retries=3 --health-timeout=10s nginx:alpine

```

### Reiniciar el contenedor en caso de fallo

```
docker run -d --name server-nginx --health-cmd="curl http://localhost" --health-interval=3s --health-start-period=5s --health-retries=3 --health-timeout=10s --restart on-failure  nginx:alpine

```

### Reiniciar el contenedor en caso se detenga manualmente

```
docker run -d --name server-nginx --health-cmd="curl http://localhost" --health-interval=3s --health-start-period=5s --health-retries=3 --health-timeout=10s --restart unless-stopped  nginx:alpine

```

### Reiniciar el contenedor en cualquier caso

```
docker run -d --name server-nginx  --health-cmd="curl http://localhost" --health-interval=3s --health-start-period=5s --health-retries=3 --health-timeout=10s --restart always  nginx:alpine

```

### Crear un contenedor temporal

```
docker run --rm -it nginx:alpine sh


```