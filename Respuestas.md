Datos Personales:

David Cabeza

# Respuestas de la Tarea 3

1. ¿Qué es un sistema de control de versiones o VCS?
El control de versiones es un sistema que graba los cambios de archivos en el tiempo para que se puedan recuperar versiones específicas posteriormente. El sistema de control de versiones más utilizado en el mundo es git. Otro sistema de versiones conocido es Mercurial.

2. ¿Qué es un repositorio?
Un repositorio es una estructura de disco que guarda meta-datos (datos sobre datos) para un conjunto de archivos o una estructura de directorios. Algunos de los metadatos que incluye un repositorio son:
- Un record histórico de los cambios en el repositorios
- Una serie de objetos de tipo commit
- Un conjunto de referencia para objetos commit, llamados heads.

3. ¿Qué es Git? ¿Qué es Github?
Git un sistema de control de versiones distribuido gratuito y de código abierto que está diseñado para manejar proyectos pequeños o grandes con velocidad y eficiencia.
Por otra parte, Github es una plataforma en línea para la gestión de repositorios remotos basados en control de versiones a través de internet. Mayormente es utilizado para código de computadoras. Ofrece todas las funcionalidades de sistemas de control de versiones distribuidos y manejo de código fuente que tiene Git.
Provee colaboración entre equipos para el desarrollo de proyectos, tracking de bugs, entre otras cosas.

5. En la terminología convencional de Git, ¿qué significa master? ¿qué significa origin?
La rama maestra es la rama por defecto que crea Git cuando se crea un repositorio y se refiere a la rama principal. La rama maestra se entiende como la rama que contiene los últimos cambios del repositorio, es decir la versión más actualizada.
Origin por otra parte, es el nombre que le da Git al repositorio remoto en donde todos los miembros del equipo hacen push. No necesariamente el repositorio remoto se tiene que llamar origin pero es el nombre que git le da por defecto. 

6. ¿Cómo se inicializa un repositorio en Git?
Primeramente se ubica en el directorio donde se quiere inicializar el repositorio y a través del comando git init crea la carpeta necesaria para el control de versiones.

7. ¿Cómo se clona un repositorio en Git?
A través del comando git clone <ruta_repositorio>

8. ¿Qué es un remote? ¿Cómo se añade un nuevo remote a un repositorio?
Un remote es una versión del proyecto que se encuentra alojada en Internet o en una red en alguna parte. Se pueden tener varias de estas, donde cada una generalmente puede ser de sólo lectura o de lectura y escritura. El manejo de remotes es esencial para la colaboración entre equipos de trabajo en proyectos.