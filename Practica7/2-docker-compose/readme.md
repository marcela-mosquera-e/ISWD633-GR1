## Docker Compose

Docker Compose permite definir la configuración de todos los servicios de una aplicación en un solo archivo **compose.yaml**.
- Cada servicio se ejecuta en su propio contenedor. 
- Facilita la gestión y el mantenimiento de la configuración, en comparación con la gestión de múltiples archivos de configuración de Docker o scripts de shell. 
- Ayuda a tener consistencia en los entornos de desarrollo, pruebas y producción.

## Ejercicio
El archivo compose.yaml permitirá configurar dos servicios de acuerdo con el siguiente esquema:

![Escenaio docker compose](escenario-docker compose.png)

**Completar el archivo compose.yaml, solamente en las partes que solicta <valor>**


**Archivo Docker Compose**
En este archivo  se define los servicios que componen la aplicación. 
Cada servicio puede incluir la imagen a usar, los puertos a exponer, los volúmenes a montar y otras configuraciones.

### Ejecutar Docker compose
Si algún servicio no se creó correctamente se puede usar
el comando descargará las imágenes necesarias, creará y ejecutará los contenedores según lo definido en el archivo compose.yaml
Para ejecutar en modo "detached" (en segundo plano) se agrega la opción -d:
```
docker compose up -d <nombre contenedor>
```

### Ejecutar Docker compose
Este comando descargará las imágenes necesarias, creará y ejecutará los contenedores según lo definido en el archivo compose.yaml
Para ejecutar en modo "detached" (en segundo plano) se agrega la opción -d:
```
docker compose up -d
```