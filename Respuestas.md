# Santiago Rodríguez
## 1511257
## santo1996.29@gmail.com

### 1. ¿Qué es un VCS?

Es un sistema que registra cambios en un archivo o conjunto de archivos a lo largo del tiempo y asi tener la posibilidad de recuperar
versiones específicas posteriormente.

### 2. ¿Qué es un repositorio?

Un repositorio, depósito o archivo es un sitio centralizado donde se almacena, organiza, mantiene y difunde información digital, habitualmente bases de datos o archivos informáticos.

### 3. ¿Qué es Git? ¿Qué es Github?

Git es una pieza de software que se encarga de modelar los datos como un conjunto de instantáneas de un minisistema de archivos. Cada vez que
confirmas un cambio, o guardas el estado de tu proyecto en Git, él básicamente hace una foto del aspecto de todos tus archivos en ese momento,
y guarda una referencia a esa instantánea. Si los archivos no se han modificado, Git no almacena el archivo de nuevo, sólo un enlace al archivo
anterior idéntico que ya tiene almacenado.

La mayoría de las operaciones en Git sólo necesitan archivos y recursos locales para operar. Por los general no se necesita información de
ningún otro servidor de tu red, es decir, todo ocurre en una base de datos local que git utiliza y luego ésta es comparada con la base de datos
remota.

Todo en Git es verificado mediante una suma de comprobración antes de ser almacenado, y es identificado a partir de ese momento mediante dicha
suma.

Git tiene tres estados principales en los que se pueden encontrar tus archivos: confirmado (commited), modificado (modiffied), y preparado
(stagged). Confirmado significa que los datos se encuentran almacenados de forma segura en tu base de datos local. Modificado significa que has
modificado el archivo pero todavía no los has confirmado a tu base de datos. Preparado significa que has marcado un archivo modificado en su
versión actual para que vaya en tu próxima confirmación.

Esto nos lleva a las tres secciones principales de un proyecto de Git: el directorio de Git (Git directory), el directorio de trabajo (working
directory), y el área de preparación(staging area).

El directorio de Git es donde Git almacena los metadatos y la base de datos de objetos para tu proyecto. El directorio de trabajo es una copia
de una versión del proyecto. El área de preparación es un sencillo archivo, generalmente contenido en tu directorio de Git, que almacena
información acerca de lo que va a ir en tu próxima confirmación.

El flujo de trabajo básico en Git es algo así:

1. Modificas una serie de archivos en tu directorio de trabajo.
2. Preparas los archivos, añadiéndolos a tu área de preparación.
3. Confirmas los cambios, lo que toma los archivos tal y como están en el área de preparación, y almacena esas instantáneas de manera permanente
en tu directorio de Git.

Github es una plataforma de desarrollo de software para alojar proyectos utilizando el sistema de control de versiones Git. Github aloja tu
repositorio de código y te brinda herramientas muy útiles para el trabajo en equipo, dentro de un proyecto.

### 4. Explica qué funcionalidad tienen los siguientes comandos de Git. Si los comandos tienen flags, mencione alguna de ellas.

- git init

    Crea un repositorio de Git vacío o reinicializa uno existente. Uno de sus flags es **-q**, el cual cumple con la función de que al emitir
    la orden sólo se muestran mensajes de advertencia y de error, los demás mensajes serán suprimidos.

- git clone

    Clona un repositorio en un nuevo directorio. Uno de sus flags es **-o <nombre>**, lo cual especifica de que en lugar de usar **origin**
    para mantener el rastro del repositorio _upstream_, use **<name>**.

- git branch

    Lista, crea, o elimina _branches_. Con el flag **--list** lista las ramas en el repositorio.

- git checkout

    Intercambia ramas o restaura archivos del árbol de trabajo. Uno de sus flags es **-f**, en presencia de este flag, al momento de cambiar
    ramas, procede incluso si el índice o el árbol de trabajo difiere de HEAD, este flag es usado para tirar al botadero cambios locales.

- git commit

    Registra los cambios al repositorio. Uno de sus flags es **-a**, lo cual añade los cambios al área de preparación de los archivos conocidos
    y luego los confirma.

- git reset

    Reinicia el HEAD actual al estado especificado. Uno de sus flags es **--soft** el cual vuelve al estado especificado sin cambiar el árbol
    de archivos.

- git pull

    Obtener e integrar con otro repositorio o de una rama local. Uno de sus flags es **-v** que pasa el flag **-v** a **git fetch**
    y a **git-merge**.

- git push

    Actualiza las referencias remotas en conjunto con los objetos asociados. Con el flag **-all** realiza **push** a todas las ramas.

- git status

    Muestra el estado del árbol de trabajo. Con el flag **-s** muestra la salida en formato corto.

- git merge

    Une dos o más historiales de desarrollo. Con el flag **--commit** realiza la unión y luego confirma los cambios.

- git log

    Muestra los registros de confirmaciones. Con el flag **--max-count=<numero>** limita el número de confirmaciones a mostrar.

- git reflog

    Maneja la información de la referencia de registros. Con el flag **--all** procesa los _reflogs_ para todas las referencias.

- git rebase

    Toma todos los cambios realizados en una rama y los reaplica sobre otra. Con el flag **--stat** muestra un _diffstat_ sobre lo que ha
    cambiado _upstream_ desde el último _rebase_.

- git remote

    Gestiona el conjunto de repositorios rastreados. Con el flag **-v** muestra el URL remoto luego del nombre.

### 5. ¿En la terminología convencional de Git, ¿qué significa master? ¿Qué significa origin?

En Git **master** simboliza la rama por defecto, luego de realizar la primera confirmación esta rama master apunta a dicha confirmación.
Al clonar de un repositorio remoto **origin** es el nombre de dicho repositorio por defecto.

### 6. ¿Cómo se inicializa un repositorio en Git?

Con **git init <dirname>** crea un directorio que cumple el papel de repositorio local. Para iniciar un repositorio en un gestor de repositorios
en línea se deben seguir los pasos descritos en tal gestor de repositorios en línea.

### 7. ¿Cómo se clona un repositorio en Git?

Con **git clone [dirname]** para clonar el repositorio bajo un directorio con el nombre **[dirname]**, es opcional, cabe destacar, en caso de
que no se le pase **[dirname]** Git crea un directorio bajo el nombre que tiene el repositorio en el gestor de repositorios en línea.

### 8. ¿Qué es un remote? ¿Cómo se añade un nuevo remote a un repositorio?

Un remote es un repositorio en línea al cual Git enviará los cambios realizados en el repositorio local de manera que se vean reflejados en el
repositorio en la red, cuando un crea un repositorio en línea, luego es necesario ir al directorio en el que se ha inicializado Git, el
repositorio local, y luego añadir el _remote_ con **git remote add <_remote_name_> <url>**.

### 9. ¿Qué es una rama? ¿Cómo se crea una rama en Git?

Una rama en Git es un apuntador que hace referencia a confirmaciones realizadas con anterioridad, _master_ por defecto. Para crear una rama
en Git se usa **git branch <branch_name>** para crear un apuntador a la confirmación más reciente con el nombre **<branch_name>**. Es necesario
recalcar que Git posee un apuntador especial llamado **HEAD** que apunta a la rama en la que Git se encuentre actualmente.

### 10. ¿Cómo subo al servidor remoto una rama que he creado localmente?

Suponiendo que la nueva rama se llama **branch_new** y ya has realizado una confirmación, sólo que realizar un **git push origin branch_new**.

### 11. ¿Cómo descargo a mi repositorio local una rama que existe en el servidor remoto pero que no tengo localmente?

Haría un **git checkout -b origin/branch_name** y luego **git pull origin brach_name**.

### 12. ¿Qué es un pull?

Sincronización del repositorio local con el repositorio remoto, actualiza la base de datos local en función de la remota y luego realiza los
cambios pertinentes según la última confirmación.

### 13. ¿Qué es un push?

Parecido a pull, con la excepción de que los datos del repositorio remoto se sincronizan con los del repositorio local, y luego los cambios
realizados en el repositorio local se ven reflejados en el repositorio remoto.

### 14. ¿Qué es un merge? ¿Cómo se realiza?

Un _merge_ se realiza para fusionar ramas en la rama actual a la que apunta **HEAD**, suponiendo que uno actualmente se encuentra en una
rama denominada **test_branch** en la que se hacen una serie de modificaciones a partir del punto de creación de **test_branch** y luego se
desea aplicar los cambios en la rama **master**, para realizar tal cometido uno luego de confirmar los cambios se mueve a la rama **master**
con **git checkout master** y luego se realizaría un **git merge test_branch**.

### 15. ¿La operación merge es conmutativa?

Pues si, una _merge_ fusiona la o las ramas especificadas sobre la rama actual a la que apunta **HEAD**.

### 16. ¿Qué es un fork?

un _fork_ es una copia de un repositorio de tal manera que uno es el dueño de la copia y es posible entonces realizar cambios a voluntad,
luego, si se desea sugerir la realización de los cambios en el repositorio original se realizaria un _pull request_ al dueño del repositorio 
original.

### 17. ¿Qué es un pull request?

Una solicitud que realiza un colaborador de algún repositorio con un fork del repositorio para que sus cambios se vean reflejados en el
repositorio original, el pull request es rechazado o aceptado por el dueño del repositorio.

### 18. ¿Qué es un commit? ¿Cómo se identifica un commit?

Un commit es la manera de confirmar los cambios realizados en la base de datos principal de Git, dichos cambios se aplicarán a los archivos
confirmados para las modificaciones, para hacer un commit luego de añadir los cambios a la zona de preparación, es es necesario emitir el
siguiente comando: **git commit -m "Cambiado README.md"** donde el flag **-m** especifica la etiqueta que identificará a la confirmación
realizada al revisar el **git log**.

### 19. ¿Qué es un merge conflict?

Son escenarios que ocurren debido cuando la rama actual y la rama que se desea fusionar con la rama actual divergen, se tienen commits en la
rama actual que no están en la otra rama y viceversa.

### 20. ¿Qué es Git flow?

Es una estrategia de gerencia de _releases_ y de _git branching_ que ayuda a los desarrolladores a mantener un rastro de las características,
_hotfixes_ y _releases_ en proyectos de software grandes. **git-flow** es solo un empaquetado de comandos de **git** existentes, éste se encarga
de manejar las ramas por uno.
