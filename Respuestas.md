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
