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

### 3-.Crea un contenedor con el nombre 'dam_ubu1'. ¿Como puedes acceder a él?

+ Creamos un contenedor sin nombre usando `DOCKER RUN -DIT --NAME dam_ubu1 UBUNTU BASH`, y podremos reacceder al contenedor usando `DOCKER EXEC -IT dam_ubu1 BASH`.

```bash
  > docker run -dit --name dam_ubu1 ubuntu bash

  > docker exec -it dam_ubu1 bash
```


