Andrea Reyes
Tarea 3

1.	¿Qué es un sistema de control de versiones o VCS?
Es una herramienta que permite manejar y registrar los cambios que se van realizando en uno o varios archivos a lo largo de su proceso de desarrollo, lo que facilita el posterior acceso a las diferentes versiones que se tienen del documento
2.	¿Qué es un repositorio?
Es un servidor centralizado en el que se almacenan documentos y archivos de un proyecto, a los cuales se puede acceder fácilmente. También permite añadir la información que se produce durante el tiempo de vida del proyecto. Los repositorios pueden ser públicos o privados.
3.	¿Qué es Git? ¿Qué es Github?
Git es un programa de código abierto de control de versiones que se utiliza para llevar un registro de los cambios que se producen en las distintas versiones de las aplicaciones, así como para acoplar y organizar los trabajos que se realizan en los archivos compartidos.
Gituhub es una plataforma de control de versiones basada en el sistema Git, para alojar proyectos que permite la colaboración de diferentes personas en los archivos que los constituyen. Se pueden alojar proyectos de forma pública o privada.
4.	Explica qué funcionalidad tienen los siguientes comandos de git. Si los comandos tienen flags, mencione alguna de ellas:
•	git init: útil para crear un repositorio vacío. Flags: --quiet, --bare, 
•	git clone: funciona para clonar un repositorio, es decir, crear una copia en el computador. Flags: --local, --shared, --s, -- quiet, --mirror.
•	git branch: nos muestra una lista de todas las ramas que están en el repositorio. Flags: --delete, --force, --m, --move, --copy, etc.
•	git checkout: funciona para ir de una rama a otra o actualizar los archivos en un árbol de trabajo. Flags: --ours, --theirs, --track.
•	git commit: registra los cambios en el repositorio. Flags: --all, --a, --p, --patch, --branch.
•	git reset: reestablece el HEAD según lo que se especifique. Flags: --q, --quiet-
•	git pull: actualiza la información de un archivo que está en el repositorio local con la que se encuentra en el remoto. Flags: --q, --quiet, --edit, -- ff-only, signoff. 
•	git push: funciona para actualizar en el repositorio los cambios que realizamos.Flags: --all, --tags, --delete, -- force.
•	git status: muestra un registro de todos los archivos que han sido modificados. Flags: --short, --branch, long, etc.
•	git merge: incorpora los cambios de los commits en la rama actual. Flags: --commit, --no-commit, --edit, --no-edit
•	git log: muestra un registro de los commits realizados. Flags: --follow, ---no-decorate, --source, entre otros.
•	git reflog: funciona para especificar el valor que anteriormente tenía una referencia. Flags: --all, --updateref, --rewrite, etc.
•	git rebase: recopila los commits que se realizaron en una rama y los aplica de nuevo. Flags: --quit, --merge, --edit-todo, entre otras.
•	git remote: administra los repositories remotos. Flags: --v, --verbose.
5.	En la terminología convencional de Git, ¿qué significa master? ¿qué significa origin?
Se denomina master a la rama de desarrollo predeterminada, es decir, al crear un repositorio, se crea la rama master que, generalmente, almacena el desarrollo local. 
Se denomina origin a las ramas de seguimiento remoto que por defecto almacenan las actualizaciones ascendentes de un repositorio. Generalmente los proyectos contienen al menos un proyecto antecesor que pueden rastrear.
6.	¿Cómo se inicializa un repositorio en Git?
Para inicializar un repositorio Git se utiliza el comando git init. Este comando crea básicamente un directorio .git con subdirectorios para guardar todo lo relativo al repositorio; así como un archivo HEAD referente al de la rama principal.
7.	¿Cómo se clona un repositorio en Git?
El comando git-clone es el que se utiliza para clonar un repositorio, es decir, crea un repositorio en un directorio nuevo y crea ramas de cada una de las que tiene el repositorio clonado, las cuales se pueden seguir remotamente.
8.	¿Qué es un remote? ¿Cómo se añade un nuevo remote a un repositorio?
Remote es un comando que administra y rastrea repositorios remotos, es decir, versiones del proyecto que se encuentran alojados en la red. Para añadir un remote a un repositorio se utiliza el comando remote add con los parámetros del repositorio.
9.	¿Qué es una rama? ¿Cómo se crea una rama en Git?
Una rama es una versión paralela de un repositorio, en la cual se puede trabajar sin afectar las otras versiones del proyecto a pesar de estar contenida en el mismo repositorio. Para crear una rama nueva en Git se usa el comando git branch <nombre de la rama>, por ejemplo: $ git branch proyecto
10.	¿Cómo subo al servidor remoto una rama que he creado localmente?
Para publicar una rama local, esta debe ser llevada a un servidor remoto donde se tenga permiso de escritura, para ello se ejecuta el comando git push (nombre remoto) (nombre rama) se puede subir al servidor remoto una rama local.
11.	¿Cómo descargo a mi repositorio local una rama que existe en el servidor remoto pero no tengo localmente?
Es necesario crear una rama local con el mismo nombre de la remota, para ello se utiliza el comando git branch <nombre rama>. Una vez creada, hay que acceder a ella a través del comando git checkout <nombre rama> y desde allí actualizar el contenido de dicha rama usando el comando git pull <nombre rama>.
12.	¿Qué es un pull?
Pull hace referencia al momento en el que se fusionan los cambios que se están realizando en el proyecto. De esta forma, las modificaciones de los archivos remotos podrán acoplarse con la copia local, así esta copia siempre estará actualizada.
13.	¿Qué es un push?
Push se refiere a enviar los cambios realizados localmente a un repositorio remoto, de manera que todos los colaboradores tengan acceso a estas modificaciones que fueron realizadas en el proyecto. 
14.	¿Qué es un merge? ¿Cómo se realiza?
Merge toma los cambios de una rama y los aplica a otra. Este comando es utilizado por git pull para incorporar cambios desde otro repositorio y puede usarse manualmente para fusionar los cambios de una rama a otra.
15.	¿La operación de merge es conmutativa?
No es conmutativa. 
16.	¿Qué es un fork?
Es una copia del repositorio original que es totalmente independiente del mismo. Se obtienen dos repositorios iguales, sin embargo, las modificaciones que se realizan en uno de ellos no afecta al otro. 
17.	¿Qué es un pull request?
Un pull request es una solicitud que el propietario de un fork de un repositorio hace al propietario del repositorio original para que los commits que están en el fork sean añadidos, es decir, que los cambios realizados en el repositorio externo se incluyan en el principal.
18.	¿Qué es un commit? ¿Cómo se identifica un commit?
Un commit es la acción de guardar los archivos de un proyecto en un repositorio remoto o local.
19.	¿Qué es un merge conflict?
Es un conflicto que ocurre cuando las ramas que se desean fusionar divergen. Es decir, que una haya commits que no se encuentran en la otra.
20.	¿Qué es Git flow?
Es una extensión de git que favorece el manejo de las ramas y los flujos de trabajos


