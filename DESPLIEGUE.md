# Cambios realizados en el repositorio
1. Modificamos el archivo `index.html` ubicado en la ruta: `./src/main/resources/templates/` añadiendo nuestro nombre en las etiquetas `<title></title>` y la etiqueta `<h1></h1>` (cambiar la etiqueta `<p></p>` del footer es opcional).
![](./assets/img/Captura%20desde%202025-12-07%2016-29-16.png)
2. Montamos la imagen de docker con el comando `docker compose up -d` y comprobamos si los cambios se han aplicado en el `localhost`
![](./assets/img/Captura%20desde%202025-12-07%2016-40-45.png)
3. una vez hayamos comprobado que se hayan aplicado los cambios debemos crear un archivo de Github actions
![https://github.com/ricitos2001/2526_DAW_u2_springboot/blob/816e813936ff8b2555b97117a82afa8f0cb41ddd/.github/workflows/workflow.yml#L1-L29]
4. Vamos al repositorio y accedemos a la parte de configuracion. Despues accedemos a la parte donde pone variables y secretos y creamos dos secretos del repositorio uno con tu nombre de usuario de docker y otro con la contraseña de tu usuario de docker. Si no lo haces es posible que el workflow falle
![](./assets/img/Captura%20desde%202025-12-07%2016-38-08.png)
5. 