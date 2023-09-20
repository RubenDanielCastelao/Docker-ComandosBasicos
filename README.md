# Docker-ComandosBasicos


### 1-.Descarga la imagen 'ubuntu y comprueba que está en tu equipo

+ Descargamos la imagen de ubuntu usando `DOCKER PULL UBUNTU`, y luego comprobamos que el proceso se haya realizado correctamente usando `DOCKER IMAGES`.

```bash
  > docker pull ubuntu

  > docker images
```
### 2-.Crea un contenedor sin ponerle nombre. ¿está arrancado? Obtén el nombre

+ Creamos un contenedor sin nombre usando `DOCKER RUN -DIT UBUNTU BASH`, y luego vemos el nombre con `DOCKER PS`. El nombre que se le da al contenedor será aleatorio, en este caso "**gracious_tu**".

```bash
  > docker run -dit ubuntu bash

  > docker ps
```

