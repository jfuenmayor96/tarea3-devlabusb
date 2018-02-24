

Nairelys Hernández 12-10199

1) Sistema de Control de Versiones

Es un sistema que permite llevar una bitácora de cambios sobre un archivo para que la recuperación de alguna versión del mismo pueda ser realizada sin inconveniente.

2) Un repositorio...

Un repositorio es un lugar donde guardar, organizar y mantener los archivos.

3) Git y Github

Git es un sistema de control de versiones distribuido, es decir, cada colaborador conserva una copia de seguridad de manera que si el servidor muere , la información de cualquier colaborador puede ser copiada en el servidor. Además de que es posible tener varios flujos de trabajos en caso de trabajar con diferentes grupos en el mismo proyecto y así evitar intromisiones y conservar un orden.

Github es un servicio que permite trabajar bajo repositorios gestionados por el sistema de control de versiones.

4) Comandos de Git:

 	- `git init` inicializa git en la carpeta donde se ejecuta
  - `git clone` Usado para clonar un repositorio
  - `git branch` Usado para crear y manejar ramas
  - `git checkout` Usado para manejarse entre ramas, es decir, manejar el head
  - `git commit`
        -m carga en el head los cambios realizados 
        -a agregar en el head los cambios
        --amend se refiere al último commit sin generar uno nuevo
  - `git reset` Usado  para dar marcha atrás a alguna acción
  - `git pull` Actualiza el repositorio local 
  - `git push` se hacen efectivos las actualizaciones sobre los archivos especificados
  - `git status`Lista un estado actual del repositorio con lista de archivos modificados o agregados
  - `git merge` Usado para fusionar la rama actual con alguna otra
  - `git log`Muestra los logs de los commits
        --oneline --stat Muestra los cambios en los commits
        --oneline --graph Muestra gráficos de los commits 
  - `git reflog` Se refiere aun historial que conserva los cambios que va teniendo el puntero head
  - `git rebase` Usado para actualizar las ramas con respecto a la rama principal sin afectarla
  - `git remote` Se usa para manejar repositorios remotos
 5) Master y origin

 En el entorno de git, se usa master para referirse a la rama principal cuando se hacer git init y se usa origin para referirse al repositorio remoto cuando se utiliza git clone.

 6) Inicializando un repositorio en Git 
 Para inicializar un repositorio en Git se debe usar el comando git init, esto genera un repositorio nuevo .git.

 7)Clonar un repositorio
 Esto se lleva a cabo con el comando git clone seguido de la dirección del repositorio que se quiera clonar

 8)Remote

 remote sirve para visualizar los repositorios remotos que tenemos en el servidor y poder manejarlos

 9,10, 11) Ramas - Branch
 	Una rama es un flujo nuevo diferente a la rama original, los cambios hechos es esta no afectan la rama principal ni otras ramas ya creadas.

 	Para generar un rama nueva se usa el comando git branch seguido del nombre de la nueva rama
 12) Pull
   Se usa git pull para actualizar el repositorio local con los últimos cambios realizados en el repositorio remoto
 13) Push
  Hacer push se refiere a subir cambios desde el repositorio local al repositorio remoto
 14) ¿Qué es un merge? ¿Cómo se realiza?
  El merge incorpora cambios en la rama master, decir, fusiona una rama con la rama principal. 
 15) ¿La operación de merge es conmutativa?
  
 16) Merge
  Cuando se realiza un fork se genera un nuevo repositorio en tu cuenta de git con una nueva dirección y contiene los
  mismos archivos que el repositorio sobre el que se ha aplicado el fork.
 17) ¿Qué es un pull request? 
   Es un apetición realizada para que las actualizaciones que tiene un fork sean incorporadas al repositorio original.
 18) ¿Qué es un commit? ¿Cómo se identifica un commit?
   Un commit identifica los cambios registrados en un archivo, los cuales son identificados con un serial único y su id apunta hacia sus padres.
 19) ¿Qué es un merge conflict?
  Sucede cuando se hacen diferentes acciones que resultan contradictorias sobre un mismo archivo , lo que provoca que git no 
  encuentre la forma de decidir que acción es la adecuado por lo que amerita mas ordenes de parte del usuario
 20) ¿Qué es Git flow? 
  Es una metodología de trabajo que divide las secciones del proyecto en ramas para que resulte más fácil su manejo y las 
  posibles incorporaciones 
