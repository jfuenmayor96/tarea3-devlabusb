**Nombre:** Alejandro Salazar
**Carnet:** 16-11080

**¿Qué es un sistema de control de versiones?**
Es una herramienta que registra todos los cambios hechos en un proyecto, guardando asi sus diferentes fases de progreso, y permite que nos movamos hacia atrás o hacia adelante en estas diferentes versiones.

**¿Qué es un repositorio?**
Es el lugar donde se almacena la historia (diferentes versiones) de un proyecto.

**¿Qué es Git? ¿Qué es GitHub?**
Git es el sistema de control de versiones moderno más usado actualmente. Es un proyecto open source creado en 2005 por Linus Torvalds, el creador del kernel de Linux. Git es distribuido, es decir, en vez de tener un sólo lugar para la historia del proyecto , en Git la copia del proyecto que tiene cada desarrollador es también un repositorio que contiene toda la historia de cambios.
Github es una plataforma de desarrollo colaborativo de software para alojar proyectos utilizando el sistema de control de versiones Git.

 - `git init`: inicializar git en la carpeta desde la que se llama el comando o la que se especifica después. Flags: -q, --quiet, --bare, --shared.
 - `git clone`: clona un repositorio dentro de una nueva carpeta. Flags: --progress, --origin, --branch, --no-tags, --single-branch.
 - `git branch`: listar, crear o borrar ramas. Flags: --delete, --copy, --move, --force, --color, --remotes, --all, --list.
 - `git checkout`: moverse entre ramas o restaurar archivos del working tree. Flags: --branch, --merge, --orphan.
 - `git commit`: grabar cambios en el repositorio. Flags: -m, -a, --author, --date, --amend.
 - `git reset`: devuelve la cabecera actual a la fecha especificada. Flags: --soft, --mixed, --hard, --merge, --keep.
 - `git pull`: traer desde e integrar con otro repositorio o rama local. Flags: --commit, --no-commit, --edit, --no-edit, --ff.
 - `git push`: actualiza las referencias remotas usando las referencias locales, enviando los objetos necesarios para completar las referencias dadas. Flags: --all, --prune, --dry-run, --delete, --tags, 
 - `git-status`: muestra el estado del working tree. Flags: --short, --branch, --long.
 - `git merge`: Junta dos o más historias de desarrollo. Flags: --commit, --no-commit, --edit, --no-edit, --ff, --progress, -m.
 - `git log`: muestra el registro de commits. Flags: --oneline, --short, --medium, --full, --fuller, --raw, --format, -n, --skip, --since, --after, --merges, --no-merges, --branches, --tags.
 - `git reflog`: Manejar la información del reflog. Utiliza los subcomandos show, expire, delete y exists. Show acepta todos los flags aceptados por `git log`, expire acepta, entre otros: --all, --expire, --expire-unreachable, --updateref, --rewrite, --stale-fix, --dry-run. Delete acepta --updateref, --rewrite, --dry-run.
 - -`git rebase`: reaplicar todos los commits de una rama en otra. Flags: --onto, --merge, --skip-
 - `git remote`Maneja un conjunto de repositorios rastreados. 

**En la terminología convencional de Git, ¿qué significa master? ¿qué significa origin?**
"Master" es el nombre de la rama que git crea por defecto cuando se crea un repositorio por primera vez. En la mayoría de los casos, master es la rama principal. 
"Origin" es el nombre por defecto que git le da al repositorio remoto principal.

**¿Cómo se inicializa un repositorio en Git?**
Con el comando `git init`.

**¿Cómo se clona un repositorio en Git?**
Con el comando `git clone` seguido de la dirección del repositorio.

**¿Qué es un remote? ¿Cómo se añade un nuevo remote a un repositorio?**
Un remote en git es un marcador para un repositorio diferente al cual deseas hacer push o pull. Puede estar en la misma computadora en una carpeta diferente, o en un servidor remoto. Para añadir nuevos remote se utiliza el comando `git remote add` seguido del nombre remoto o una dirección URL.

**¿Qué es una rama? ¿Cómo se crea una rama en Git?**
Una rama es una versión alterna del proyecto. Efectivamente se trata de forks dentro del mismo repositorio. Las ramas tienen un commit predecesor y divergirán de dicho commit con los cambios que se le hagan. Se crean con el comando `git checkout -b` seguido del nombre de la nueva rama.

**¿Cómo subo al servidor remoto una rama que he creado localmente?**
Con el comando `git push -u origin` seguido del nombre de la rama local

**¿Cómo descargo a mi repositorio local una rama que existe en el servidor remoto pero no tengo localmente?**
Con el comando `git fetch origin` seguido del nombre de la rama.

**¿Qué es un pull?**
`git pull` realiza un `git fetch` seguido de un `git merge`. Es decir, actualiza las ramas de seguimiento remoto y luego las combina con las ramas locales.

**¿Qué es un push?**
`git push` envía al repositorio remoto los cambios realizados en el repositorio local.

**¿Qué es un merge?¿Cómo se realiza?**
Un merge incorpora los cambios realizados sobre una rama (desde el momento en que divergieron) en la rama actual. Se realiza con el comando `git merge` seguido del nombre de la rama que se combinara con la rama actual.

**¿La operación de merge es conmutativa?**
En cuanto al contenido de la rama resultante, puede ser conmutativa dependiendo de como se manejen los conflictos, sin embargo desde el punto de vista de la historia del proyecto no, no es conmutativa.

**¿Qué es un fork?**
Un fork es una copia exacta en crudo de un repositorio original. Es decir, después del fork, tendremos 2 repositorios exactamente iguales pero con distinta URL. Estos dos repositorios son completamente autónomos el uno del otro, los cambios que se efectúen en el original no se transmiten al fork ni viceversa. Se utiliza para poder contribuir con proyectos dentro de git sin haber sido designado como contribuidor, o para iniciar nuevos proyectos en base a proyectos ya existentes.

**¿Qué es un pull request?**
Un pull request es una petición que el propietario de un fork de un repositorio hace al propietario del repositorio original para que este último incorpore los commits que están en el fork.

**¿Qué es un commit? ¿Cómo se identifica un commit?**
Un commit es un registro que contiene todos los cambios realizados al proyecto hasta la creación del commit. 

**¿Qué es un merge conflict?**
Los merge conflict ocurren cuando al hacer merge, un mismo archivo presenta diferentes modificaciones en cada una de las ramas. Git es capaz de resolver estos problemas en la mayoría de los casos pero si, por ejemplo, en una rama se borra una línea mientras en la otra se modifica, git no sabe cuál version es la correcta, por lo que aparece un merge conflict.

**¿Qué es Git flow?**
Git Flow es un proceso para manejar cambios creado por Vincent Driessen y acompañado de extensiones de git para manejarlo.La idean general detrás de git flow es tener diferentes rama que siempre existen, cada una con un propósito diferente: master, develop, feature, release, y hotfix. El proceso de desarrollo de funcionalidades o el arreglo de bugs se desplaza de una rama a la otra hasta ser publicado.

