# Restart

**Para esta práctica**
Se van a crear imágenes para probar cada una de las políticas de reinicio.
Analice las instrucciones de cada Dockerfile 
Use la imagen respectiva para crear y ejecutar el contenedor y observar lo que sucede verificando 
el cumplimiento de la política de reinicio.

### restart = no

No reinicia el contenedor bajo ninguna razón

### restart = always

Si se detiene manualmente, no se reinicia. El contenedor es iniciado nuevamente cuando el demonio (servicio) reinicia

```
docker run -d --name <nombre contenedor> --restart always <nombre imagen>
```

### restart = unless-stopped

Se reinicia siempre y cuando no se detenga manualmente

```
docker run -d --name <nombre contenedor> --restart unless-stopped <nombre imagen>
```

### restart = on-failure

Se reinicia únicamente cuando hay una falla en la ejecución del código. No se reinicia si el contenedor se detiene manualmente.

```
docker run -d --name <nombre contenedor> --restart on-failure <nombre imagen>
```
