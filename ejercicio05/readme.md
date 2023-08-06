## Respuestas

### HealthChecks

Dockerfile Healthcheck es una opción del sistema que se encarga de indicarle al daemon de Docker cómo comprobar que el contenedor se encuentre funcionando, es decir, le dice cómo probar un determinado container de Docker para verificar si aún se encuentra realizando sus labores.

Esta instrucción permite que el sistema sea capaz de detectar casos de errores, como, por ejemplo, un servidor web que esté atascado en un bucle infinito y que no pueda controlar las conexiones nuevas, incluso si el proceso de este servidor sigue ejecutándose dentro de la plataforma.

### Onbuild

La instrucción ONBUILD añade a la imagen una instrucción de activación que se ejecutará más adelante, cuando la imagen se utilice como base para otra compilación. El disparador se ejecutará en el contexto de la compilación posterior, como si se hubiera insertado inmediatamente después de la instrucción FROM en el archivo Dockerfile posterior.

ONBUILD es útil para imágenes que se van a construir desde (FROM) una imagen dada. Por ejemplo, podrías usar ONBUILD para una imagen de pila de lenguajes que construye software de usuario arbitrario escrito en ese lenguaje dentro del Dockerfile, como puedes ver en las variantes ONBUILD de Ruby.

### Volume

Los volúmenes son el mecanismo preferido para la persistencia de los datos generados y utilizados por los contenedores Docker. Mientras que los bind mounts dependen de la estructura de directorios y del sistema operativo de la máquina anfitriona, los volúmenes están completamente gestionados por Docker. Los volúmenes tienen varias ventajas sobre los bind mounts:

1. Los volúmenes son más fáciles de respaldar o migrar que los bind mounts.
2. Puedes gestionar los volúmenes utilizando los comandos CLI de Docker o la API de Docker.
3. Los volúmenes funcionan tanto en contenedores Linux como Windows.
4. Los volúmenes pueden compartirse de forma más segura entre varios contenedores.
5. Los controladores de volumen permiten almacenar volúmenes en hosts remotos o proveedores de nube, cifrar el contenido de los volúmenes o añadir otras funcionalidades.
6. Los nuevos volúmenes pueden tener su contenido pre-poblado por un contenedor.
7. Los volúmenes en Docker Desktop tienen un rendimiento mucho mayor que los montajes bind desde hosts Mac y Windows.

Además, los volúmenes son a menudo una mejor opción que la persistencia de datos en la capa de escritura de un contenedor, porque un volumen no aumenta el tamaño de los contenedores que lo utilizan, y el contenido del volumen existe fuera del ciclo de vida de un contenedor determinado.
