# Examen del tercer trimestre
# DOCKER

# Ejercicio 1
## Ejemplo 1
### Vamos a utilizar el comando *docker pull ubuntu:18.04* para descargar una imagen del sistema operativo Ubuntu version 18.04.

[![imagen-2022-06-13-093504403.png](https://i.postimg.cc/1zRK15rh/imagen-2022-06-13-093504403.png)](https://postimg.cc/BjyFx3zM)

### Mediante el comando *docker run -it ubuntu:18.04 /bin/bash* crearemos un contenedor en base a la imagen que hemos descargado previamente es decir un contenedor de Ubuntu version 18.04 (Si nos hemos saltado el paso anterior la imagen se descargara) en la captura se puede ver como una vez ejecutado me encuentro dentro de este contenedor.

[![imagen-2022-06-13-093757872.png](https://i.postimg.cc/sXXK7DM9/imagen-2022-06-13-093757872.png)](https://postimg.cc/mcvQG4Nt)

## Ejemplo 2
### Utilizaremos el comando *docker run centos ls /* para  crear un contenedor en base a la imagen de centOs ademas que al aplicarle el *ls* nos listara el contenido de la carpeta de este mismo y el contenedor pasa a estar parado, al no añadirle version a este comando nos descargara automaticamente la ultima existente.

[![imagen-2022-06-13-095118519.png](https://i.postimg.cc/QdBkmnm1/imagen-2022-06-13-095118519.png)](https://postimg.cc/hXBdPsHt)

## Ejemplo 3
### Mediante el comando *docker run httpd* se nos creara la imagen del HTTPD y se creara un servidor Web Apache 2.4 en la ip mostrada, una vez creado se nos mostrara en la misma terminal el log de dicho servidor.

[![imagen-2022-06-13-095912552.png](https://i.postimg.cc/T3FSJs8W/imagen-2022-06-13-095912552.png)](https://postimg.cc/21d2z2Sz)

## Ejemplo 4
### Mediante el comando *docker run -it -w /etc debian:9 ls*  nos creara una imagen de debian version 9 en caso de que aun no la tengamos y ademas al añadirle el parametro *-w* y especificando que carpeta queremos en este caso */etc* nos mostrara el contenido de esta carpeta una vez creado el contenedor.

[![imagen-2022-06-13-100653786.png](https://i.postimg.cc/Vv3Ss1rF/imagen-2022-06-13-100653786.png)](https://postimg.cc/ctB1TpcK)

### Para finalizar vamos a ver 2 comandos basicos de mostrar el estado de los contenedores

### Mediante el comando *docker ps* mostraremos los contenedores que se encuentran en ejecución, en mi caso como no se encuentra ninguno en ejecucion no me mostrara nada.

[![imagen-2022-06-13-101141835.png](https://i.postimg.cc/tJYjSxgr/imagen-2022-06-13-101141835.png)](https://postimg.cc/vxFkDDf9)

### Mediante el comando *docker ps -a* mostraremos todos los contenedores creados tanto si estan en ejecucion como si estan parados.

[![imagen-2022-06-13-101402815.png](https://i.postimg.cc/tgp7rBG2/imagen-2022-06-13-101402815.png)](https://postimg.cc/fVqwyjL9)

# Ejercicio 2

## Mediante el comando *vi adriandockerfile* creamos nuestro propio dockerfile

[![imagen-2022-06-13-103713650.png](https://i.postimg.cc/7Y9M4tqJ/imagen-2022-06-13-103713650.png)](https://postimg.cc/w7tscVy9)

[![imagen-2022-06-13-103749367.png](https://i.postimg.cc/Hn25pj11/imagen-2022-06-13-103749367.png)](https://postimg.cc/BPjtpSvm)

## Una vez dentro colocaremos lo que aparece por la imagen dentro del dockerfile y lo guardamos.

[![imagen-2022-06-13-105748023.png](https://i.postimg.cc/tgt7bmxn/imagen-2022-06-13-105748023.png)](https://postimg.cc/B8bJcpNJ)

## Realizamos un tag mediante el comando *docker build --tag dockerfile*

[![Captura-de-pantalla-2022-06-13-105511.png](https://i.postimg.cc/y8nYrS40/Captura-de-pantalla-2022-06-13-105511.png)](https://postimg.cc/LJYpJ5ss)

## Realizamos un tag a la imagen (importante poner nuestro usuario de dockerhub)

[![imagen-2022-06-13-110306765.png](https://i.postimg.cc/SR8cWfP6/imagen-2022-06-13-110306765.png)](https://postimg.cc/m1Lc4CBk)

## Realizamos un push a docker hub mediante el comando *docker push adrianmartinn/dockerfile*

[![imagen-2022-06-13-110542229.png](https://i.postimg.cc/Wpr9mGgY/imagen-2022-06-13-110542229.png)](https://postimg.cc/Z0bF4yf6)

## Comprobamos que se ha subido a docker hub

[![imagen-2022-06-13-110739347.png](https://i.postimg.cc/nhYbd8m5/imagen-2022-06-13-110739347.png)](https://postimg.cc/cvHbHbXM)






