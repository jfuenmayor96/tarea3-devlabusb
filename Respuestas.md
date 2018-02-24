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

4. Explica qué funcionalidad tienen los siguientes comandos de git. Si los comandos tienen flags, mencione alguna de ellas:
`git init` → crea un repositorio de git vacío o inicializa de nuevo uno existente. El flag -q sirve para que el comando se comporte de manera silenciosa imprimiendo solo errores y advertencias.
`git clone` → clona un repositorio en un directorio nuevo. 
`git branch` → lista, crea o elimina ramas de git. El flag -d elimina una rama.
`git checkout` → cambio de ramas o recuperación de archivos de árboles de trabajo. -b crea una nueva rama.
`git commit` → registra cambios al repositorio. -m se utiliza para especificar el mensaje del commit.
`git reset` → resetea el HEAD actual al estado especificado. --hard resetea el índice actual y el árbol de trabajo.
`git pull` → recupera e integra desde otro repositorio o una rama local. -v para que la salida sea verbosa. También tiene unos flags asociados a los merges como --commit.
`git push` → actualiza las referencias remotas a lo largo de los objetos asociados. --all hace push de todas las ramas.
`git status` →muestra el estado del árbol de trabajo. -s da la salida del estatus en formato acortado.
`git merge` →une dos o más historias de desarrollo. --commit se usa para hacer el merge y hacer commit del resultado.
`git log` → muestra logs (registros) de los commits. --follow continúa listando la historia de un archivo más allá de los renombramientos (solo funciona para un archivo específico)
`git reflog` →reflog se refiere a logs de referencia y estos registran cuando las “puntas” de las ramas y otras referencias fueron actualizadas en el repositorio local. Es útil en varios comandos de git para especificar el valor anterior de una referencia. Este comando maneja estos logs.
`git rebase` → vuelve a aplicar commits en la parte superior de la punta de otra base.
`git remote` → administra un conjunto de repositorios “rastreados”

5. En la terminología convencional de Git, ¿qué significa master? ¿qué significa origin?
La rama maestra es la rama por defecto que crea Git cuando se crea un repositorio y se refiere a la rama principal. La rama maestra se entiende como la rama que contiene los últimos cambios del repositorio, es decir la versión más actualizada.
Origin por otra parte, es el nombre que le da Git al repositorio remoto en donde todos los miembros del equipo hacen push. No necesariamente el repositorio remoto se tiene que llamar origin pero es el nombre que git le da por defecto. 

6. ¿Cómo se inicializa un repositorio en Git?
Primeramente se ubica en el directorio donde se quiere inicializar el repositorio y a través del comando `git init` crea la carpeta necesaria para el control de versiones.

7. ¿Cómo se clona un repositorio en Git?
A través del comando `git clone <ruta_repositorio>`

8. ¿Qué es un remote? ¿Cómo se añade un nuevo remote a un repositorio?
Un remote es una versión del proyecto que se encuentra alojada en Internet o en una red en alguna parte. Se pueden tener varias de estas, donde cada una generalmente puede ser de sólo lectura o de lectura y escritura. El manejo de remotes es esencial para la colaboración entre equipos de trabajo en proyectos. Con el comando `git remote add <nombre_remoto> <direccion del remoto>`

9. ¿Qué es una rama? ¿Cómo se crea una rama en Git?
Dentro de un repositorio se tienen ramas las cuáles se pueden ver como “forks” dentro del mismo repositorio. Las ramas tendrán un commit ancestro en el repositorio y divergirán de ese commit con los cambios que se hagan en ella. Posteriormente, se pueden mezclar los cambios de las ramas. Las ramas permiten trabajar en varias características que no tienen que ver una con la otra a la vez. Con el comando git checkout -b <nombre_de_la_rama> se crea la rama y se cambia automáticamente a esta.

10. ¿Cómo subo al servidor remoto una rama que he creado localmente?
Si el remoto es origin, a través del comando `git push -u origin <nombre_de_la_rama>` se envía al servidor remoto la rama creada.

11. ¿Cómo descargo a mi repositorio local una rama que existe en el servidor remoto pero no tengo localmente?
A través del comando git fetch se obtienen todas las ramas que se han creado en el servidor remoto. Fetch no actualiza las ramas locales, si se desean actualizar estas se debe hacer pull de las ramas.

12. ¿Qué es un pull?
Incorpora cambios de un repositorio remoto en la rama actual. En su modo predeterminado, `git pull` es la abreviatura de git fetch seguido de git merge FETCH_HEAD.

13. ¿Qué es un push?
Cuando se hace un push, se están enviando al servidor remoto todos los commits que se tienen locales al momento de ejecutar el comando.

14. ¿Qué es un merge? ¿Cómo se realiza?
Merge se refiere a mezclado. Un merge ocurre cuando varias personas (dos o más) hicieron cambios sobre un mismo archivo. En ese caso, el sistema de control de versiones debe mezclar todos los cambios lo cual normalmente se hace por una estrategia recursiva, existen otros algoritmos de merge como el “Three way merge”, Fuzzy Patch application, Weave merge, entre otros. Puede ocurrir que dos personas hicieron cambios sobre un mismo segmento del archivo lo cual resulta en un merge conflict en el cual se incluyen mediante unas etiquetas las partes que resultaron en el conflicto y debe ser solucionado manualmente.

15. ¿La operación de merge es conmutativa?
Lo es para merges por defecto. Si dos ramas B y C son hijas de un ancestro en común A. Mezclar B en C debe producir el mismo resultado que mezclar C en B. Pero no se puede decir lo mismo en el caso de (B en C) en A contra B en (C en A). El merge

16. ¿Qué es un fork?
Un fork es una copia de un repositorio. El fork permite experimentar libremente realizando cambios sin afectar el proyecto original. 
Comúnmente, los forks se utilizan para proponer cambios al proyecto de otra persona o para usar el proyecto de otra persona como punto de partida para su propia idea.

17. ¿Qué es un pull request?
Los pull request permiten informar a otros acerca de los cambios que se han enviado a un repositorio en GitHub. Una vez que se abre un pull request se puede analizar y discutir los posibles cambios con los colaboradores y agregar commits de seguimiento antes de que los cambios se mezclen en el repositorio (merge).

18. ¿Qué es un commit? ¿Cómo se identifica un commit?
Un commit almacena el contenido actual del índice en un objeto commit junto con un mensaje de registro del usuario que describe los cambios. Un commit se identifica por un hash. Por ejemplo, según git log, el hash de mi último commit al momento de escribir esta pregunta fue bd190c4071f613ba4738c9e41800e8c075aa94fa

19. ¿Qué es un merge conflict?
Algunas veces git puede resolver diferencias entre ramas mezcladas. Por lo general, los cambios se realizan en diferentes líneas, o incluso en diferentes archivos, lo que hace que la fusión sea simple para que las computadoras entiendan esta. Sin embargo, a veces hay cambios competitivos en los que Git necesita ayuda para decidir qué cambios incorporar en la fusión final. A menudo, los conflictos de combinación ocurren cuando las personas hacen cambios diferentes en la misma línea del mismo archivo, o cuando una persona edita un archivo y otra persona elimina el mismo archivo. Debe resolver el conflicto antes de poder fusionar las ramas.

20. ¿Qué es Git flow?
Es un modelo creado por Vincent Driessen que ayuda a simplificar el desarrollo y la gestión de lanzamientos (releases). El modelo es útil en un flujo de trabajo de gestión de versiones para empresas. En este modelo un repositorio tiene dos ramas principales:

Master, la cual es una rama altamente estable que siempre está lista para producción y contiene la última versión de lanzamiento del código fuente.

Develop, que se deriva de la rama master. La rama de desarrollo sirve como una rama para integrar diferentes características planificadas para un lanzamiento que está por venir. Esta rama puede o no puede ser tan estable como la rama master. En esta rama, los desarroladores colaboran y mezclan las subramas con características.

Además de estas dos ramas principales, existen otras ramas en el modelo de trabajo

Feature, que se deriva de la rama develop y es utilizada para desarrollar características.

Release, que también se deriva de develop pero es utilizada durante lanzamientos.

Hotfix, esta se deriva de la rama master y es utilizada para resolver bugs en la rama de producción que fueron identificados después de un lanzamiento.