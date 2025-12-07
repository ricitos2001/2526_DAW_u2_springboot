# Cambios realizados en el repositorio
1. Modificamos el archivo `index.html` ubicado en la ruta: `./src/main/resources/templates/` añadiendo nuestro nombre en las etiquetas `<title></title>` y la etiqueta `<h1></h1>` (cambiar la etiqueta `<p></p>` del footer es opcional).
![](./assets/img/Captura%20desde%202025-12-07%2016-29-16.png)
2. Montamos la imagen de docker con el comando `docker compose up -d` y comprobamos si los cambios se han aplicado en el `localhost`
![](./assets/img/Captura%20desde%202025-12-07%2016-40-45.png)
3. una vez hayamos comprobado que se hayan aplicado los cambios debemos crear un archivo de Github actions
![https://github.com/ricitos2001/2526_DAW_u2_springboot/blob/816e813936ff8b2555b97117a82afa8f0cb41ddd/.github/workflows/workflow.yml#L1-L29]
4. Vamos al repositorio y accedemos a la parte de configuracion. Despues accedemos a la parte donde pone variables y secretos y creamos dos secretos del repositorio uno con tu nombre de usuario de docker y otro con la contraseña de tu usuario de docker. Si no lo haces es posible que el workflow falle
![](./assets/img/Captura%20desde%202025-12-07%2016-38-08.png)

Una vez realizado todo hacemos un push a nuestro repositorio para poder realizar los cambios y si lo hemos hecho bien todo deberia aparecernos esto en la pestaña de github actions:
![](./assets/img/Captura%20desde%202025-12-07%2017-01-37.png)
![](./assets/img/Captura%20desde%202025-12-07%2017-01-37.png)

Ademas de esto deberiamos ver nuestra imagen subida en Docker Hub
![](./assets/img/Captura%20desde%202025-12-07%2017-03-37.png)
![](./assets/img/Captura%20desde%202025-12-07%2017-04-57.png)


## Detalles a tener en cuenta
Tuve que cambiar el puerto en el archivo `docker.compose.yml` ya que por alguna extraña razon el puerto 8080:8080 ya estaba en uso
![https://github.com/ricitos2001/2526_DAW_u2_springboot/blob/c4e3f39d9bcd35bf7fb60f960e3539b94acfa346/docker-compose.yml#L1-L48]
Para descargaros la imagen debeis usar el siguiente comando
`docker push ricitosdeoro2001/springboot-crud-app:latest`

Para poder ejecutarla utilizareis este otro comando:
`
docker run -d --name springboot-crud-app ricitosdeoro2001/springboot-crud-app:latest
`
Si lo prefieres hacer con un archivo de docker.compose.yml solo tienes que cambiar el nombre de la imagen actual por este otro: `ricitosdeoro2001/springboot-crud-app:latest`

## Utilidades
Instrucciones de la aplicacion de springboot: [README.md](./README.md)
Enlace a la imagen de docker: [ricitosdeoro2001 - springboot-crud-app](https://hub.docker.com/repository/docker/ricitosdeoro2001/springboot-crud-app/general)
Archivo docker.compose.yml: [docker.compose.yml](docker-compose.yml)
Archivo del workflow: [workflow.yml](.github/workflows/workflow.yml)
