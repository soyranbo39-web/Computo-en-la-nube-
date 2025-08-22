# Tarea docker 
# Instrucciones
Entregar un repositorio de GIT que contenga:

dockerfile: este archivo deberá crear una imagen de aplicación que corra apache o nginx en el puerto 80, donde la interfaz deberá mostrar la palabra "Hola Cómputo en la nube".

Deberán utilizar los comandos de docker para crear la imagen y lanzar o deploy esta imagen localmente en sus equipos. Deberán poner estos comandos en el archivo README.md

Adjuntar como entregable un screenshot del Repositorio.
La entre será presencial el 22 de Agosto.


Este proyecto crea una aplicación web simple que muestra el mensaje "Hola Cómputo en la nube" utilizando Docker.


## Archivos del Proyecto

- **index.html**: Contiene el código HTML que muestra la interfaz de la aplicación.
- **Dockerfile**: Define la imagen de Docker, instala y configura Apache o Nginx, y copia el archivo `index.html` al directorio adecuado.


**Creación del Dockerfile**
   
   Se creó un archivo llamado `Dockerfile` con las siguientes instrucciones:
   - Se eligió una imagen base oficial de Apache (`httpd:2.4`).
   - Se copió el archivo `index.html` al directorio adecuado de Apache (`/usr/local/apache2/htdocs/`).
   
   Ejemplo de Dockerfile:
   dockerfile
   FROM httpd:2.4
   COPY index.html /usr/local/apache2/htdocs/index.html
   

 **Construcción de la imagen Docker**
   
   Desde la terminal, se navegó al directorio del proyecto y se ejecutó el comando:
   
   docker build -t docker-web-app .
   
   Esto crea una imagen llamada `docker-web-app` usando el Dockerfile.

**Ejecución del contenedor**
   
   Para iniciar la aplicación, se ejecutó:
   
   docker run -d -p 80:80 docker-web-app
   
   Esto inicia un contenedor en segundo plano y expone el puerto 80 del contenedor en el puerto 80 de la máquina local.



## Comandos Utilizados


# Construir la imagen
docker build -t docker-web-app .

# Ejecutar el contenedor
docker run -d -p 80:80 docker-web-app



