
## Tarea 3 Admisión Devlab
## Yuni Quintero



**1. ¿Qué es un sistema de control de versiones o VCS?**

Control de versiones es utilizado para administrar múltiples versiones de archivos y programas. Un sistema de control de versiones o VCS provee dos capacidades principales para la administración de datos. Le permite al usuario bloquear archivos para que sólo puedan ser editados por una persona a la vez, y, rastrear los cambios a los archivos.



**2. ¿Qué es un repositorio?**

En desarrollo de software, un repositorio es una ubicación de almacenamiento de archivos central. Es utilizado por sistemas de control de versiones para almacenar múltiples versiones de archivos. Mientras un repositorio puede ser configurado en una máquina local para un sólo usuario, la mayoría de las veces es almacenado en un servidor, el cual puede ser accedido por varios usuarios.

Un repositorio provee una manera estructurada a los programadores de almacenar archivos de desarrollo. Esto puede ser útil para cualquier tipo de desarrollo de software, pero es especialmente importante para grandes proyectos de desarrollo.



**3. ¿Qué es Git? ¿Qué es Github?**

Git es un sistema de control de versiones gratuito y open-source diseñado para manejar tanto proyectos pequeños como grandes. Git permite tener múltiples branches que pueden ser idependientes entre sí. 

Github es un hosting service para control de versiones que utiliza Git. Se utiliza comunmente para códigos de programación. Provee funciones de control de versiones distribuidas y administracion de codigo fuente de Git.



**4. Explica qué funcionalidad tienen los siguientes comandos de git. Si los comandos tienen flags, mencione alguna de ellas:**

+ `git init`: crea un repositorio Git vacio o reinicializa uno ya existente
flags: `--quiet, --bare, -q`
+ `git clone`: clona un repositorio en un nuevo directorio
flags: `-l, -s, --mirror`
+ `git branch`: lista, crea o elimina branches
flags: `--no-color, --list, --no-column`
+ `git checkout`: cambia entre branches o restablece working tree files
flags: `-q, -f, -m`
+ `git commit`: registra los cambios del repositorio
flags: `--interactive, --amend, --dry-run`
+ `git reset`: reinicia la HEAD actual al estado especificado
flags: `-q, --patch, --soft, --hard`
+ `git pull`: extraer e integrarse con otro repositorio o branch local
+ `git push`: actualizar referencias remotas junto con objetos asociados
flags: `--all, --force, --delete, --atomic`
+ `git status`: muestra el estado actual del working tree
+ `git merge`: fusionar uno o mas ramas dentro de la rama activa
flags: `--stat, --abort, --continue`
+ `git log`: muestra los commits
+ `git reflog`: muestra una lista ordenada de los commits que apunta HEAD
+ `git rebase`: hacer rebase a una branch mueve completamente la rama con la nueva característica hacia la HEAD del master
flags: `--interactive, --exec, --skip`
+ `git remote`: para ver qué repositorios remotos se tienen configurados
flags: `--verbose`



**5. En la terminología convencional de Git, ¿qué significa master? ¿qué significa origin?**

Master es la rama por defecto de Git. Con la primera confirmación de cambios que se realicen, se creará esta rama principal master.

Origin hace referencia a un repositorio remoto particular. No es propiedad del repositorio.

Si uno se encuentra en la rama master y copia los cambios a un repositorio remoto (push), se encontraran ahora en el repositorio remoto para que otros usuarios accedan a él. En el repositorio local otra rama llamada `origin/master` se crea la cual hace referencia al servidor de la rama remota. `origin/master` siempre intenta estar al día con respecto al repositorio de la rama remota.



**6. ¿Cómo se inicializa un repositorio en Git?**

Mediante el comando `$ git init`, esto crea un subdirectorio llamado .git que contiene todos los archivos necesarios del repositorio. Con `git add` se especifica que archivos se desean controlar, seguidos de un `commit` para confirmar los cambios.



**7. ¿Cómo se clona un repositorio en Git?**

Mediante el comando `git clone` y anexando en la misma linea el URL del repositorio github. `git clone [url]`



**8. ¿Qué es un remote? ¿Cómo se añade un nuevo remote a un repositorio?**

Los repositorios remote son versiones de un proyecto que estan hospedados en el internet o en alguna red. Se añade un nuevo remote a un repositorio mediante el comando `git remote add [shortname] [url]`, el url del repositorio respectivo a agregar.



**9. ¿Qué es una rama? ¿Cómo se crea una rama en Git?**

Una rama en Git es un apuntador móvil y liviano que apunta a un commit. La rama por defecto en Git es `master`. Cuando se realizan los primeros cambios, es dado una rama master que apunta al ultimo commit hecho.

Cuando se crea una nueva rama se crea un nuevo apuntador para uno poder moverse. Esto se lleva a cabo mediante el comando `git checkout -b [nombre rama]`.
El cual es un atajo de `git branch [nombre rama]` `git checkout [nombre rama]`


**10. ¿Cómo subo al servidor remoto una rama que he creado localmente?**

Mediante el comando `git push [nombre remoto] [nombre rama]`


**11. ¿Cómo descargo a mi repositorio local una rama que existe en el servidor remoto pero no tengo localmente?**

Mediante el comando `git fetch [remoto]`



**12. ¿Qué es un pull?**

Incorpora cambios de un repositorio remoto a la rama actual, mediante el comando `git pull`



**13. ¿Qué es un push?**

Actualiza referencias remotas utilizando refrencias locales, enviando objetos necesarios para completar las referencias dadas. Mediante el comando `git push`



**14. ¿Qué es un merge? ¿Cómo se realiza?**

Incorpora cambios desde los commits a una rama actual. Mediante el comando `git merge`



**15. ¿La operación de merge es conmutativa?** No, pueden existir problemas de sobrescritura.



**16. ¿Qué es un fork?**

Al contribuir en un proyecto existente al que uno no tiene acceso para hacer push, uno puede hacer "fork" al proyecto, GitHub creará una copia del proyecto propia para uno, a este se le puede hacer push y todo tipo de operaciones. De esta manera, los proyectos no tiene que añadir a usuarios como colaboradores para darles acceso al push.



**17. ¿Qué es un pull request?**

Los demás usuarios pueden hacerle fork a un proyecto, pushearlo y contribuir sus cambios de vuelta al repositorio original mediante la creación de lo que se llama un Pull Request. Esto genera una solicitud a un proyecto para permitir que este haga pull a su árbol.



**18. ¿Qué es un commit? ¿Cómo se identifica un commit?**

Funciona para guardar cambios en el repositorio, para confirmar de manera instántanea esos cambios al repositorio cada vez que el proyecto alcance un estado que se desee grabar. Se realiza mediante el comando `git commit -m "mensaje"` 

El identificador de un commit es un hash SHA-1 que contiene todo lo importante referente a un commmit como su contenido, fecha de commit, el nombre de quien realizó el commit y su dirección email, el mensaje log y el ID del commit previo.



**19. ¿Qué es un merge conflict?**

Ocurre por varios casos, cuando se edita una línea de archivo y al mismo tiempo se le hizo un cambio externo, o cuando un archivo es eliminado y otra persona intentaba editarlo. Cuando se realizan cambios y se solicitan `merge`, si el estado del archivo original cambia durante este proceso, ocurre un conflicto.



**20. ¿Qué es Git flow?**

Es un conjunto de extensiones de git que proveen operaciones de alto nivel sobre operaciones. Define un modelo estricto de ramas. Está basado en la idea de Git workflow. Dicta qué tipo de ramas se configuran y como fusionarlas juntas.