## Instrucciones

1. Descargar la imagen `docker image pull nicopaez/pingapp:3.0.0`

2. Renombramos la imagen descargada con la información del nuevo repositorio `docker tag nicopaez/pingapp:3.0.0 luzho/ejercicio02:0.0.1`

3. Hacemos `docker login` para asegurarnos que tenemos las credenciales al repo que queremos hacer push de la imagen, ingresamos nuestras credenciales de docker hub.

4. Luego subimos la imagen al repo con el siguiente comando `docker push luzho/ejercicio02:0.0.1`

5. El comando para descargar la imagen del nuevo repo seria la siguiente: `docker image pull luzho/ejercicio02:0.0.1`