## Instrucciones para build y ejecución

 1. Construir la imagen nginx:
```shell
	docker build -t ejercicio01:0.0.1 .
```
 2. Ejecutar la imagen:
 ```shell
	docker run -d -p 8080:80 ejercicio01:0.0.1
```
3. Abrir en cualquier navegador lo siguiente: `http://localhost:8080/`