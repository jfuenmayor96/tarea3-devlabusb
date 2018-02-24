## 1) ¿Qué es un sistema de control de versiones o VCS?
Es un software que ayuda a los desarrolladores mantener un control de los
distintos cambios que ha tenido un proyecto.

## 2) ¿Qué es un repositorio?
Es un lugar donde guardar los códigos fuentes, entre otros documentos, de un
programa.

## 3) ¿Qué es Git? ¿Qué es Github?
Git es un VCS creado por Linus Torvalds, conocido por todos los programadores,
que facilita la colaboración de varios desarrolladores en un solo programa.
GIthub es una interfaz web de Git, hecha principalmente para alojar repositorios
de proyectos open source.

## 4) Explica qué funcionalidad tienen los siguientes comandos de git. Si los comandos tienen flags, mencione alguna de ellas:
### `git init`:
Este comando crea un repositorio git vacío.
#### Algunos flags:
1. `-q`: solo imprime errores y advertencias. El resto del output será ignorado.

### `git clone`:
clona un repositorio en un nuevo directorio, crea ramas que siguen
remotamente a las ramas del repositorio clonado.
#### Algunos flags:
1. `--reference <repositorio>`:
Si el repositorio referenciado está en la máquina local, automáticamente setea
`/git/objects/info/alternates` para obtener objetos del repositorio referenciado.

2. `-v`: Corre verbosamente.

###`git branch`:
 Lista, crea o borra ramas.

#### Algunos flags:
1. `-d`: borra una rama.
2. `-m`: Mueve/renombra una rama.
3. `-c`: copia  una raama.

### `git checkout`
Cambia entre ramas o restaura los archivos del working tree.
#### Algunos flags:
1. `-q`: Suprime mensajes de feedback.
2. `-b`: Crea una nueva rama.

### `git commit`:
Registra cambios al repositorio.
#### Algunos flags:
1. `-a`: automáticamente mueve al index archivos que han sido modificados o borrados, pero nuevos archivos que no les has informado a Git no serán afectados.
2. `-p`: Usa la interfaz interactiva para escoger cuales cambios commitear.
3. `-branch`: Muestra la rama e información del tracking.

### `git reset`:
Resetea el actual HEAD (apuntador a la rama o estado actual en el que se trabaja) a un estado especifico.
#### Algunos flags:
1. `-q`: Solo reporta erroes.
2. `--soft <commit>`: No toca el archivo de index or el working tree para nada, pero resetea el HEAD a <commit>. Mantiene todos tus cambios.
3. `--mixed <commit>`: Resetea el index pero no el working tree. Todos los cambios desde <commit> son descartados.
4. `--hard <commit>`: Reseta el index y working tree. Cualquier cambio después de <commit> es descartado.
5. `--merge <commit>`: Resetea el index y actualliza los archivos en el working tree que son diferentes entre <commit> y HEAD, pero mantiene auqellosque son diferentes entre el index y el working tree.
6. `--keep`: Resetea el inde y actualzia archivos en el working tree que son diferentes entre <commit> y HEAD.

### `git pull`:
Extrae desde e integra con otro repositorio o rama local.
#### Algunos flags:
1. `-q`: Solo muestra los errores.
2. `-v`: Pasa `--verbose` a git-fetch y git-merge
3. `--commit`: Realiza el merge y commitea el resutlado.
4. `--ff`: Cuando el merge resuelve con un fast-forward, solo actualiza el puntero de la rama, sin crear un commit de merge. Este es el comportamiento por defecto.
5. `--no-ff`: Crea un commit de merge incluso cuando el merge termina en un fast-forward.

### `git push`:
Actualiza las referencias remotas con los objetos asociados.
#### Algunos flags:
1. `<repositorio>`: El repositorio remoto destino.
2. `--all`: Pushea todas las ramas.
3. `--prune`: Remueve las ramas remotas que no tienen una contraparte local.

### `git status`:
Muestra el estatus del working tree.
#### Algunos flags:
1. `-s`: Devuelve el output en un formato corto.
2. `-b`: Muestra la rama e información de seguimiento incluso en formato corto.
3. `--long`: Devuelve un output en formato largo. Este es el comportamiento por defecto.

### `git merge`:
Une dos o más historias juntas.
#### Algunos flags:
1. `--commit`: Realiza el merge y comitea el resultado.
2. `-ff`: Cuando el merge resuelve como un fast-forward, solo actualiza el apuntador de la rama, sin crear un commit para el merge. Este es el comportamiento por defecto.
3. `--no-ff`: Crea un commit de merge incluso cuando el merge resuelve como un fast-forward.

### `git log`:
Muestra los logs de los commits.
#### Algunos flags:
1. `--source`: Imprime el naombre de la referencia en la linea de comandos por el cual cada commit fue alcanzado.

### `git reflog`:
A diferencia de `git log`, este muestra solo los commits a los que HEAD a apuntado.
#### Algunos flags:
1. `--all`: Procesa los reflogs de todas las referencias.
2. `--verbose`: Imprime información extra.

### `git rebase`:
A diferencia de `git merge`, este reaplica los cambios de la rama actual en otra rama, desde el ancestro común "más joven". Útil para "aplanar" el repositorio.
#### Algunos flags:
1. `--onto <nueva base>`: Punto de inicio de donde se empezará a crear los nuevos commits.
2. `<branch>`: Rama a utilizar. Por defecto es HEAD.
3. `--continue`: Reinicia la reorganización después de resolver un conflicto de merge.

### `git remote`:
Maneja el conjunto de repositorios seguidos.
#### Algunos flags:
1. `-v`: Imprime información adicional, incluyendo url remoto después del nombre.
#### Comandos:
1. `add <name> <url>`: Agrega un remoto con nombre <name> con la URL <url>.
2. `rename <old> <new>`: Renombra el remoto nombra <old> a <new>/
3. `remove <name>`: Remueve el remoto nombrado <name>.

##  5) En la terminología convencional de Git, ¿qué significa master? ¿qué significa origin?
**master** es la rama principal del repositorio, la que es asignada para las versiones oficiales, listas para producción o las que unen todos los cambios realizados por todos los contribuyentes al proyecto.
**origin** corresponde al nombre que se le da al repositorio remoto del cual se clonó o se subió el repositorio.
