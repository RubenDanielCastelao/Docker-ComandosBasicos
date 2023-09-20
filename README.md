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

### 4-.Comprueba que ip tiene y si puedes hacer un ping a google.com

+ Realizamos el comando `ifconfig`, para comprobar la ip de el contenedor, que es en este caso: **172.17.0.3**, y hacemos `ping google.com` comprobando, que el ping es posible, pero funciona con tiempos mucho mayores que el PC principal.

```bash
  > ifconfig

  > ping google.com
```

### 5-.Crea un contenedor con el nombre 'dam_ubu2'.¿Puedes hacer ping entre los contenedores?

+ Creamos el contenedor **dam_ubu2** con este comando `DOCKER RUN -DIT --NAME dam_ubu2 UBUNTU BASH`, y luego hacemos el ping a **dam_ubu1** desde este nuevo contenedor usando `PING 172.17.0.3`, comprobando que el retraso de ping es muy bajo. de menos de 0.05ms.

```bash
  > docker run -dit --name dam_ubu2 ubuntu bash

  > ping 172.17.0.3
```

### 6-.Sal del terminal, ¿que ocurrió con el contenedor?

+ Al crearlo con -dit el contenedor se mantiene junto a todo los cambios hechos en este

