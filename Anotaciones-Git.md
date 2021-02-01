# Anotaciones Git y GitHub

## Instalación
 - Ir a la página de [Git](https://git-scm.com/) y descargar la última versión de Git que se encuentre disponible para el sistema operativo.        

 - En el caso de Windows hay que aceptar el acuerdo de licencia, en la siguiente pestaña en la parte de **Windows Explorer integration** deben estar marcadas las casillas ***Git Bash Here y Git GUI Here***, en la siguiente pestaña se debe marcar la opción ***Use Git from the Windows Command Prompt***, en la siguiente pestaña se deja marcada la opción ***Use the OpenSSL library***, en la siguiente pestaña se deja la opción por defecto ***Checkout Windows-style, commit Unix-style line endings***, en la siguiente pestaña se deja seleccionado la primera opción ***Use MinTTY (the default terminal of MSYS2)***, en la siguiente pestaña se deja todo por Default (las primeras dos opciones son las que vienen marcadas), finalmente se presiona **Install** y se espera a que se instale.

## Fundamentos

- Git funciona como una máquina del tiempo que permite saber todos los cambios realizados a los archivos del repositorio.

- Un proyecto en Git es equivalente a un repositorio. Existen dos repositorios, Central y Distribuido.

    - **Central:** Es donde existe un solo repositorio en el cual el equipo de desarrollo trabaja.

    - **Distribuido:** Es donde cada    integrante del equipo de desarrollo tiene un una copia del repositorio en las cuales cada uno de ellos irá trabajando, luego de trabajarlos todos los cambios se unen en el repositorio que funge el trabajo de centralizar todos los cambios realizados por los integrantes del equipo de trabajo.

### ¿Cómo funciona Git?

Git es como una línea de tiempo que guarda **commits** los cuales se pueden interpretar como "screenshots" del código. Git permite que uno pueda ver el "screenshot" de cual sea el momento en que se tomó.

### Primeros Comandos

- **Git Help:** El comando `git help `entrega información sobre los comandos que se pueden utilizar. En el caso de que se quiere más información sobre un comando se puede utilizar el siguiente comando `git help "comando"` el cual entrega más información sobre el "comando" (debe ir sin comillas) seleccionado. En el caso de que la información sea muy extensa, en el fondo se podrán observar dos puntos `:`, en el caso de que pase eso sólo se debe presionar la letra Q para salir de ahí y volver a la consola.

- **Git Config:** El comando `git config` permite la configuración del usuario que utilizará Git en la maquina. Los comandos básicos a utilizar son dos `git config --global user.name nombre del usuario` y `git config --global user.email mail del usuario` **(nombre del usuario y mail del usuario deben ser reemplazados por el nombre y mail del usuario)** los cuales sirven para establecer el nombre de usuario y el mail del usuario que utilizará Git en la máquina. El hacerlo de forma de global significa que cada vez que alguien haga un commit desde la sesión de la máquina en la cual se configuro el usuario, el commit llevará el nombre y mail del usuario.
Para poder ver los cambios hechos se utiliza el comando `git config --global -e`, al presionar enter se verá el nombre y mail del usuario. Para salir se debe teclear *:q* y enter. En el caso de que **se quiera restablecer un valor agregado con `git config --global`** se debe utilizar el comando `git config --global --unset variable-a-cambiar`. 

Cabe destacar que **dentro de un repositorio**, se puede utilizar `git config user.email mail-usuario` y `git config user.name nombre-usuario` (o sea que los comandos de configuración sin el *--global*) configurando asi el mail y usuario solamente para el repositorio. 

### Iniciando un proyecto y creación de repositorio

Antes de comenzar hay que estar ubicado en la carpeta del proyecto.

- El primer comando a utilizar es `git init` el cual inicializará el proyecto en Git creando un repositorio vacío. Al utilizar `git init` se crea una carpeta oculta la cual contiene todas las configuraciones del repositorio además de todo lo importante y necesario que se relacione con este. En el caso de eliminar esa carpeta, se eliminará el repositorio.

- Con el proyecto ya inicializado, se pueden comenzar a utilizar comandos tales como `git status` el cual muestra todos los archivos que git reconoce que existen en la carpeta pero que no han sido registradas en ningún lugar. Nos dice que se modificó, que es lo que está en el stage (agregado) y en que rama estamos trabajando.

- Habiendo utilizado `git status`, Git mediante el uso de `git add .` (el punto es el que hace referencia a todos los archivos) permite dar a conocer todos los archivos que contendrá el "screenshot" que se realizará a futuro. Cabe mencionar que con la información de `git status` se puede decidir que archivos se añadirán para el "screenshot" al utilizar `git add nombre del archivo` (nombre del archivo debe ser reemplazado por el nombre y la extensión del archivo que se desea añadir).

- En el caso de que se quiera resetear el add que se hizo anteriormente, se puede utilizar el comando `git reset`.

- Con los archivos ya añadidos al índice se debe realizar un "screenshot" lo cual es equivalente a utilizar el comando `git commit -m "Mensaje del commit"` el cual realiza el "screenshot" y a su vez deja ese screenshot con un mensaje **(el mensaje debe ir entre comillas en el comando)**. Cabe destacar que lo ideal es que el comentario del *commit* se encuentre en tiempo presente y haga referencia a lo que se hizo en el proyecto para que cualquier que lo lea pueda entender que fue lo que se hizo sin siquiera ver los cambios realizados.

Existe una línea del tiempo creada al momento de utilizar el comando `git init` la cual se denominará ***Master*** la cual guarda todos los commits realizados. ***HEAD*** es una especie de puntero que indica el commit en el cual estamos ubicado en la línea Master. Si volvemos a un commit anterior al último commit realizado, todo lo nuevo hecho desde el commit antiguo al commit nuevo desaparece.

- Usando el comando `git log` se pueden ver todos los commits hechos desde el más nuevo (el primero que se muestra) hasta el más antiguo (el último que se muestra), además se muestra toda la información relacionada al *commit* o sea, nombre del usuario que lo realizó, mail del usuario, fecha y hora, etc.

### ¿Qué hace Git por nosotros en estos momentos? (checkout)

Luego de los comandos utilizados anteriormente, queda responder a la pregunta propuesta en el título de esta sección.

- Primero que todo, imaginemos que dentro del código en el cual se está trabajando sin querer se guardan cambios fatales los cuales no se pueden deshacer utilizando el confiable *Ctrl+z*, Git mediante el uso del comando `git checkout -- .` (el punto hace referencia a todo) permite recuperar todo el cambio recién realizado. Si al utilizar el comando no aparece ningún mensaje, entonces el cambio se realizó correctamente. El comando tiene un alcance absurdo por lo cual se puede borrar la carpeta del proyecto y aún así con `git checkout -- .` se puede recuperar todo. **Lo anterior es posible siempre y cuando no se haya realizado un commit**.

**Si se quiere revertir los cambios de un archivo para dejarlo como estaba en cierto commit** se debe utilizar el comando `git checkout hash-del-commit nombre-del-archivo-con-extensión-incluida`, el cual hará que el archivo vuelva al estado que se encontraba en el commit que se indicó mediante su hash abreviado en el comando. Luego de haber hecho lo anterior sólo queda añadir el cambió al stage para luego hacer el commit pertinente que hable de lo que se hizo con el archivo.

### Diferentes formas de agregar archivos al escenario (stage)

Anteriormente se mencionó que con el comando `git add .` se pueden añadir a un commit todos los archivos modificados pero existen otras formas de añadir archivos a los commits las cuales veremos a continuación.

- En el caso de que **no se quiera hacer un commit con todos los archivos que existen para agregar** y sólo se quiera hacer un commit con un archivo, se debe hacer un `git add nombre-del-archivo.extensión-del-archivo` para luego hacer un commit común y corriente.

- En el caso de que se quiera **añadir al stage solamente los archivos con una misma extensión** se debe ocupar el comando `git add *.extensión-de-los-archivos` donde el asterisco hace referencia a todos los archivos que tenga le extensión señalada en el comando. Luego de realizar lo anterior se hace un commit común y corriente.

- En el caso de que se quiera **añadir todos los archivos de una sola carpeta** se debe utilizar el siguiente comando `git add carpeta\`. Luego de lo anterior se hace un commit común y corriente.

- En el caso de que se quieran **añadir todos los archivos menos uno** se puede realizar el proceso de llevar al stage **todos los archivos modificados** con el comando `git add -A` y luego **excluir los archivos que queremos dejar fuera del commit** utilizando el comando `git reset HEAD lo-que-se-quiera-excluir`. Luego de realizado lo anterior se realiza un commit común y corriente. 

- Existen otros comandos para agregar archivos al stage los cuales son:
    - `git add "*.extensión-del-archivo"`: Sirve para agregar todos los archivos del proyecto con la extensión señalada. Las camillas hacen referencia a todo el proyecto.

    - `git add *.extensión-del-archivo`: Sirve para agregar todos los archivos con esa extensión que se encuentren en el directorio en el cual estamos situados.

    - `git add --all`: Sirve para agregar absolutamente todos los archivos modificados. Es parecido al comando `git add -A`

    - `git add <lista de archivos>`: Agrega los archivos que listemos **buscar más info de este comando**

    -`git add directorio/*.extensión-del-archivo`: Agrega todos los archivos con la extensión señalada que se encuentren dentro del directorio señalado.

    - `git add directorio/`: Agrega todos los archivos que se encuentren dentro del directorio señalado.

### Otras formas de revisar el log y otra maneras de trabajar con los últimos cambios de un commit

Antes que nada hay que aclarar que el ***HEAD*** se refiere al último commit en la rama actual (línea del tiempo en la cual se está trabajando).

#### Para git log

- El comando `git log` entrega el hash completo del commit, el autor, la fecha y la descripción de lo que se hizo. En el caso de que **se quiera visualizar el hash corto del commit y la descripción del mismo** se debe utilizar el comando `git log --oneline`

- Al comando del punto anterior se le puede agregar una gran variedad de parámetros pero los más importante son:

    - `--decorate`y `graph`: Entre ambos permiten ver de manera elegante cosas. Entre más ramas existan y más grande se vuelva el proyecto, decorate y graph serán más útiles
    - `--all`: Muestra toda la información referente a las diferentes ramas y otras cosas.

Sabiendo lo anterior el comando con los nuevos parámetros quedaría de la siguiente forma `git log --oneline --decorate --all --graph`.

#### Para git status

Cabe mencionar que cuando en los parámetros del comando se ponen dos líneas (dash) antes del parámetro, significa que el parámetro a utilizar es una palabra (ejemplo de lo anterior es --online). En el caso contrario donde se utilice un sólo dash, git interpretará que cada parámetro es independiente uno del otro aunque se manden todos juntos como si fueran una sola palabra.

- Para que al momento de utilizar el comando `git status` este **nos entregue sólo los archivos modificados y los que se encuentran en el stage**, se debe utilizar el comando `git status -s` (la s es de silent). Si además de lo anterior se quiere **saber en que rama (branch) se está trabajando** se debe agregar el parámetro `-b` lo cual dejaría el comando como `git status -s -b` o como `git status -sb`.

### Alias para los comandos (shortcuts)

Anteriormente se vieron comandos muy útiles que lamentablemente son muy largos, por suerte Git ofrece la opción de crear un alias para esos comandos los cuales podrán ser utilizados de forma global. Lo anterior se hace de la siguiente manera:

- El comando con el cual se asigna el alias es `git config --global alias.el-alias-que-se-asigna-al-comando "comando-al-que-se-le-asigna-el-alias"`. Hay que tener en consideración que dentro de las comillas se debe poner todo lo que sigue después del `git` y no se debe dar un alias con el nombre de un comando ya existente. Cabe mencionar que toda la información modificada se puede encontrar utilizando el comando `git config --global -e` (-e hace referencia a edit, cuidado con editar algo directamente). Una forma más segura de ver toda la información modificada es utilizando el comando `git config --global -l` el cual sólo muestra por lo cual no hay riesgo de edición involuntaria.

## Un poco más allá de los fundamentos 

### Diferencias entre commits y restauración de archivos

- Para **saber los cambios hechos en un archivo antes de haber añadido al stage los archivos y haber realizado un commit**, se puede utilizar el comando `git diff`, el cual muestra que archivos cambiaron y cual fue el cambio en comparación a los archivos del último commit.

- Luego de **haber añadido los archivos al stage** `git diff` no mostrará nada pero si se le agrega el atributo `--staged`, ahora mostrará los cambios entre el último commit y lo que se encuentre en el stage `git diff --staged`.

- `git diff` también sirve para comparar cambios entre commits (poniendo el hash del último commit y luego el hash del commit elegido, ambos separados por un espacio) y además sirve para ver los cambios entre ramas (poniendo el nombre de la rama actual y luego el nombre de la rama con la que se quiere comparar, ambos separados por un espacio). **La información anterior es de utilidad más adelante**

- En el caso de que se **quiera revertir los cambios para dejarlo igual que en el último commit**, no debe haber nada en el stage (utilizar `git reset` para sacar del stage los archivos modificados), cumpliendo lo anterior se puede utilizar el comando `git checkout`, en el caso de que un sólo archivo haya sido modificado, se puede utilizar el comando `git checkout -- nombre-del-archivo` (las mayúsculas y minúsculas del nombre del o los archivos son importantes a la hora de ingresar el nombre del archivo al comando).

- En el caso de que se **quiera hacer un commit sin añadir al stage previamente con el comando `git add`** se puede utilizar el comando `git commit -am "comentario"` donde la `a` hace referencia a todos los archivos que han sido modificados y que git le está dando seguimiento. Lo anterior funciona sólo con archivos ya existentes en el directorio.

- Para **modificar el comentario que iba con el commit** se debe utilizar el comando `git commit --amend -m "Nuevo comentario"`

- En el caso de que se quiera **modificar el archivo del commit recién hecho (prácticamente rehacer el ultimo commit realizado)**, hay que mover el *HEAD* al commit anterior con el comando `git reset --soft HEAD^` (^ ese carácter es el que hace referencia al commit anterior), de esta forma nos movemos en la rama a un estado anterior al del commit actual.

### Preparando un repositorio para viajes en el tiempo

- En el caso de que se **ocupe el comando `git commit` sin atributos**, el commit que se realice con los archivos que previamente se encuentran en el stage podrá llevar un mensaje multilínea el cual para comenzar a editar se debe presionar la letra *a*. Para **salir del modo edición** (el que se inicia al presionar la tecla a) se debe presionar la tecla *esc*, una vez fuera del modo edición se deben guardar los cambios, para esto hay que escribir *:wq* (w de write y q de quit). Lo anterior igual aplica cuando se utiliza `git commit --amend`.

#### Viajes en el tiempo

Git permite que viajemos entre commits (viajes en el tiempo) lo cual es una forma poderosa de poder deshacer cambios realizados entre commit o añadiendo modificaciones nuevas que deberían ir en un mismo commit. Para poder hacer lo anterior es necesario conocer los comandos que sirven para eso los cuales se presentan a continuación.

##### Al pasado

 - `git reset --soft`: **Es el comando menos destructivo a la hora de volver a un commit anterior**, no modifica nada, sólo revierte el archivo al estado que estaba en el commit elegido. Para ir a algún commit anterior al comando se le debe agregar el hash del commit al que queremos volver quedando de esta manera `git reset --soft hash-del-commit`, de esta forma los archivos volverán al estado del commit seleccionado, conservando los cambios hechos después del commit y manteniéndolos en el stage. Sabiendo lo anterior este es el momento perfecto para hacer los cambios necesarios para luego realizar el nuevo commit. **Cuando se vuelva a hacer el commit, lo idea es que el mensaje que lo acompañe haga referencia a lo que se cambió en el commit anterior y a lo nuevo que se agregó**.

 - `git reset --mixed`: **Deshace los cambios que se realizaron (deja los cambios fuera del stage) entre commits**. Para hacer lo anteriormente mencionado es necesario indicar el hash del commit al que se quiere volver quedando el comando de la siguiente forma `git reset --mixed hash-del-commit`.

 - `git reset --hard`: **Deja los archivos exactamente igual a como estaban al momento del commit seleccionado, no deja ningún cambio hecho después del commit**. En resumen al utilizar este comando se debe seleccionar el hash del commit al que se quiere restaurar los archivos sabiendo que estos quedarán exactamente iguales que en ese commit. El comando con el hash queda de la siguiente forma `git reset --hard hash-del-commit`.

##### Volver desde el pasado (a un punto del ¿Presente?¿Futuro?... se entiende)

 - `git reflog`: **Git guarda un historial con los resets, commits, amends, etc., al cual se puede acceder ocupando este comando.** Sabiendo lo anterior para volver a cualquier punto de la línea de tiempo de commits, hay que buscar el hash del punto al que se quiere que HEAD apunte y ocupar el comando `git reset --hard hash-indicado`, de esta forma todo lo que se realizó hasta ese punto se restaurará por completo.

### Cambiar el nombre y eliminar archivos mediante Git

`git mv`: **Permite cambiar el nombre de un archivo** y también permite mover un archivo (mv es de move). Para cambiar el nombre primero va el archivo que se quiere modifica y luego el nuevo nombre que se le quiere dar (incluyendo la extensión del archivo). Al utilizar un `git s` (la *s* en el comando hace referencia a `status -s -b` que es la función con sus parámetros que se escribe originalmente) o un `git status`, saldrá que el archivo fue renombrado y ya se encuentra en el stage para realizar un commit.

`git rm`: **Permite eliminar un archivo**(rm hace referencia a remove). Si se usa un `git status`, se verá que la eliminación del archivo ya se encuentra en el stage en espero a concretarla mediante un commit.

### Cambiar el nombre y eliminar archivos fuera de Git

- **Al momento de renombrar un archivo mediante un método externo a Git**, Git considera que borramos el archivo anterior y creamos uno nuevo al cual no se le está dando seguimiento (a diferencia de cuando ocupábamos los comandos de git para renombrar un archivo). Debido a lo anterior es necesario utilizar el comando `git add -u` el cual **nos permite actualizar todo** para luego hacer un `git add` con el fin de agregar los cambios al stage y que a su vez Git entienda que fue un renombramiento de archivo. Con todo lo anterior listo ya se puede realizar un commit.  

- **En el caso de eliminar un archivo mediante un método externo a Git**, sólo se debe realizar un `git add -u` antes del correspondiente `git add` y el posterior `git commit -m`.

### Ignorando archivos que no deseamos

Existen archivos que no es necesario darle seguimientos mediante Git (ejemplo de esto son los archivos .log que se van generando automáticamente) o que simplemente uno no quiere que Git les de seguimiento, para ignorarlos hay que realizar lo siguiente:

- **Crear un archivo llamado** *.gitignore* (ese es su nombre y a la vez su extensión) en el cual por línea se puede agregar una expresión (archivo a ser ignorado). El archivo *.gitignore* no debe ser ignorado nunca, ya que es necesario que el proyecto sepa siempre que archivos debe ignorar. Cabe mencionar que ingresar archivo por archivo no es necesario ya que al igual que con los comandos, se puede hacer referencia a más de un archivo, las formas de hacerlo son las siguientes:

    - **Hacer referencia a todos los archivos con una misma extensión:** Lo anterior se logra escribiendo **.extensión-de-los-archivos*, el * hace referencia a todos los archivos con la extensión señalada.

    - **Hacer referencia a un directorio:** Lo anterior se logra escribiendo *nombre-del-directorio/* en el archivo .gitignore creado con anterioridad.

## Ramas, Merge (uniones), conflictos y tags

Las ramas son líneas del tiempo alternativas, las cuales son modificables sin afectar a la rama principal (Master) y que a su vez los cambios hechos en la rama pueden ser incorporados a la rama principal. Cabe mencionar que pueden existir conflictos al intentar unir las ramas, para lo anterior Git entrega opciones para solucionar problemas.

### Conceptos principales

- **Rama:** Una rama es un línea de tiempo (como las *Master*). Se utilizan cuando se quieren agregar funcionalidades a la programa sin afectar la rama principal o cuando se quiere experimentar con el programa sin afectar al programa en si.

- **Merge (Uniones):** Se utilizan cuando se quiere unir una rama a la rama principal, en estos casos Git intentará hacer la unión por nosotros desencadenando tres posibles escenarios:

    - **Fast-forward:** Se dispara cuando Git detecta que no hay ningún cambio en la rama principal y que los cambios pueden ser reintegrados de forma transparente, haciendo que los commit de esa rama formen parte de la rama principal como si nunca nos hubiéramos separados de la rama principal. Lo anterior se puede desactivar en el caso de que no se desee que pase eso.

    - **Uniones automáticas:** Es cuando Git detecta que en la rama principal existe algún cambio que las otras ramas desconocen. Al momento de intentar hacer merge Git detecta que no existen cambios en línea iguales del código por lo cual marca un punto de unión entre la rama principal y la otra rama. A diferencia del *Fast-forward*, aquí las ramas no quedan unidad como una sola.

    - **Unión Manual:** Es en la cual Git no puede hacer el merge de forma automática. Lo anterior pasa cuando en una rama distinta a la principal se hicieron cambios en las misma líneas de código que en la rama maestra en la cual se quieren unir los cambios. Al pasar lo anterior, Git avisa que debemos realizar la unión de forma manual. Luego de realizada la unión de forma manual, se crea un *merge commit* el cual es un commit que hace referencia a la unión de las ramas.

### Creación de una rama

Para crear una nueva rama se utiliza el comando `git branch rama-nombredelarama`. En el comando anterior, anteponer `rama-` antes del nombre no es necesario pero ayuda a saber que lo que creamos es una rama. Si Git no tirá ningún mensaje de error o algo por el estilo, todo está bien.
Cabe destacar que al utilizar `git branch` sin nada, el comando nos dirá las ramas que hay en el proyecto.

### Moverse a una rama

Para cambiar de rama se utiliza el comando `git checkout nombredelarama`. **Cabe destacar que `git checkout` era el comando que nos ayudaba a reconstruir el proyecto en el caso de que perdiéramos algo**. Luego de utilizado el comando, se puede utilizar el comando `git branch` para ver en la rama que nos encontramos. El comando `git status` también hace referencia a la rama en la cual uno se encuentra.

En esta rama se pueden hacer las misma cosas que se harían en la rama principal.

### Crear y moverse automáticamente a la rama

Para evitar crear la rama y luego moverse a ella, existe el comando `git checkout -b nombredelarama`, en el cual `-b` hace referencia a la creación de la rama y el resto del comando hace referencia a moverse a la rama.

### Merge Fast-Forward

**Nota:** Cabe destacar que al utilizar `git branch` sin nada, el comando nos dirá las ramas que hay en el proyecto.

1. Antes de realizar un Merge, se debe saber las diferencias entre las ramas que se quieren unir, para esto de debe utilizar el comando `git diff nombreramaactual ramaalaquesequiereunirlaramaactual`.

2. Luego de saber que cambios se hicieron, se debe volver a la rama a la cual se le quiere fusionar algo, para esto se debe utilizar el comando `git checkout ramasalaqueselequierefusionaralgo`. Cabe mencionar que si uno ve el archivo que se cambió en la otra rama, en la rama en la cual uno está ubicado actualmente, el mismo archivo se encuentra sin cambios.

Al utilizar un `git log --oneline` se pueden ver los commits realizados en las ramas y a su vez se puede observar que no existe desfase entre ramas debido a que los cambios hechos en la rama "experimental" no existen grandes cambios entre ramas (excepto el archivo en cuestión que sólo se modificó en la rama "experimental").

3. Para unir las ramas se debe utilizar el comando `git merge ramaquesequiereunir`, el cual fusiona los cambios hechos en la rama "experimental" con la rama en la que se encuentra la cabecera. Al hacer esto, los commits de la rama "experimental" fueron agregados a la rama principal y la cabecera queda apuntando a las dos ramas.

4. Luego de que ya se unieron las ramas, la rama "experimental" ya no es necesaria por lo cual paa borrarla se debe utilizar el comando `git branch -d nombredelaramaquesequiereliminar`.

### Merge Automático

**Nota:** Cabe destacar que al utilizar `git branch` sin nada, el comando nos dirá las ramas que hay en el proyecto.

1. Antes de realizar un Merge, se debe saber las diferencias entre las ramas que se quieren unir, para esto de debe utilizar el comando `git diff nombreramaactual ramaalaquesequiereunirlaramaactual`.

2. Luego de saber que cambios se hicieron, se debe volver a la rama a la cual se le quiere fusionar algo, para esto se debe utilizar el comando `git checkout ramasalaqueselequierefusionaralgo`. Cabe mencionar que si uno ve el archivo que se cambió en la otra rama, en la rama en la cual uno está ubicado actualmente, el mismo archivo se encuentra sin cambios.

Al utilizar un `git log --oneline` se pueden ver los commits realizados en las ramas y a su vez se puede observar, como si de un desfase en el tiempo se tratase, que la rama "experimental" se encuentra desfasada debido a que en la rama actual hay cambios que no se encuentran en la rama "experimental", o sea que existen cambios que se realizaron después de la creación de la rama "experimental" en la rama actual.

3. Para unir las ramas se debe utilizar el comando `git merge ramaquesequiereunir`, el cual fusiona los cambios hechos en la rama "experimental" con la rama en la que se encuentra la cabecera. Al hacer esto, los commits de la rama "experimental" fueron agregados a la rama principal y la cabecera queda apuntando a las dos ramas.

Luego de lo anterior, se puede utilizar un `git log --oneline` para ver de forma más clara en la consola la realización del merge.

4. Luego de que ya se unieron las ramas, la rama "experimental" ya no es necesaria por lo cual paa borrarla se debe utilizar el comando `git branch -d nombredelaramaquesequiereliminar`.

### Merge con conflictos

Existen ocasiones que en una rama se modificaron archivos y que a su vez, en la rama a la que se le quieren fusionar los cambios hechos en la otra rama, también se modificaron los mismos archivos de tal forma que al momento de hacer el merge, los cambios choquen entre si generando conflictos. Para solucionar un caso como el anterior es necesario realizar lo siguiente:

Cuando se realizó el merge, en la consola de comandos, Git nos notificará que existen conflictos en un archivo en especifico y nos pide que los arreglemos para luego realizar un commit con el resultado de la solución. 

*Para la resolución de los conflictos existen programas especializados como P4Merge o sublime text con algún plugin, etc.*

Al ir al archivo, se puede ver que parte del código es el problema, además muestra el cambio del archivo al cual está apuntando el HEAD y el cambio que se hizo en la rama.

Para resolver el conflicto anterior se puede:

 1. Hacer el cambio de forma manual, o sea editando el archivo que presenta el conflicto con la información que se debe mantener en él. No olvidar quitar las etiquetas creadas por Git en el archivo (lo del HEAD y el conflicto). Básicamente resolver conflictos es eliminar las etiquetas.

 2. Utilizar algún programa especializado o un plugin para el editor de código, el cual de manera gráfica nos dice cuales son los conflictos y nos permite resolverlo directamente con las sugerencias del plugin.

Ya resulto el conflicto se deben llevar los cambios al stage y realizar un commit correspondiente que haga referencia a la resolución del conflicto.

Utilizando un `git log --oneline` se puede ver de manera más gráfica en la consola de comando la resolución de conflictos y la posterior unión automática de las ramas.

**Recordar borrar la rama después de la realización del merge**.

### Tags (Etiquetas)

**Son una referencia a un commit en específico en el tiempo**. Se suelen utilizar para marcar versiones o releases de los aplicativos o programas, de esta forma se sabrá de mejor manera cual es el commit relacionado a una versión especifica del aplicativo o programa y a su vez, se podrá volver a ese commit de manera más sencilla.

#### Comandos importantes

- `git tag`: Muestra los Tags existentes de menor a mayor (pensando en que el nombre de los tags tienen que ver con versiones numéricas).
- `git tag nombredeltag`: Crea un Tag con el nombre indicado. El problema de este tag es que no da detalle de nada.
- `git tag -d nombredeltag`: Elimina un Tag. `-d`  hace referencia a deleted.

Suponiendo que uno se encuentra en en el punto en el cual quiere realizar un Tag, existe un comando para la creación de un Tag al cual se le puede añadir más información.

-`git tag -a versión -m "comentario"`: Este comando sirve para crear un tag con una anotación (la versión que es el nombre del tag) y un mensaje (lo que va entre las comillas). Ya creado el tag, si se ocupa `git log --oneline` se puede ver que en el commit donde se encuentra la cabecera es donde está el tag y ahí se quedará para siempre.

- **Si se quiere agregar un tag en un commit en el cual la cabecera no esté apuntando**, se puede utilizar el hash del commit en el comando anterior quedando de la siguiente manera `git tag -a versión hashdelcommit -m "comentario"`. 

- **Para ver el mensaje que se incluyó en el Tag** se debe utilizar el comando `git show nombredelTag`, además del mensaje se entrega información de quién hizo el Tag, hora, fecha y a que commit hace referencia junto con los cambio que se presentaron en el mismo.

## Git Stash y Git Rebase (Para realizar cambios de emergencia)

### Stash

Es como una caja en la cual se pueden guardar todos los cambios temporales (que usualmente no están completos o que su implementación puede traer problemas) con el fin de dejar el proyecto en el estado que se encontraba en un determinado commit. Lo que se encuentra guardado en la caja se puede recuperar, haciendo que el proyecto vuelva al estado que se encontraba antes de utilizar el stash.

Stash suele utilizarse cuando se están realizando cambios que todavía no están en el stage o en un commit y se necesita realizar cambios de emergencia en la rama principal que tienen más prioridad que los cambios en los que se estaban trabajando (los cuales pueden generar conflictos con el cambio de emergencia).

#### Comandos Stash

`git stash`: **Crea el stash que guarda el estado del proyecto**. En la consola al hacer un `git log --oneline` se puede observar el momento en el que se hizo el Stash. Luego de realizar un stash, todos los cambios realizados no se observan en los archivos (es como que no se hubieran hecho). En la consola se muestra *WIP on ramaactual: hashcommit Mensaje-del-commit* (WIP es Work In Progress). Se pude tener más de un stash. **Cada vez que desde un stash se restauren los cambios, se debe borrar el stash (es como lo de borrar las ramas ya utilizadas)**

Utilizar `git stash` es equivalente a utilizar `git stash save`. De todas formas, el este comando entrega otros usos como los que se mencionarán ahora:

- **Keep index:** Sirve para guardar en el stash todos los cambios menos los que ya se encuentran en el stage, esto se debe a que los cambios que se encuentren en el stage usualmente están listos para ser agregado a un commit. El comando queda así `git stash save --keep-index`.

- **Include-untracked:** Sirve para agregar todos los archivos incluyendo lo que Git no les da seguimiento. Lo anterior es de utilidad **cuando existen archivos nuevos creados los cuales Git aún no les da seguimiento**. El comando queda de esta manera `git stash save --include-untracked`.

- **Agregar un mensaje al stash:** Con el comando `git stash save "mensaje"` se puede hacer un stash que incluya un mensaje sobre las modificaciones que se estaban en haciendo (el mensaje va entre comillas).

`git stash list`: **Muestra todos los WIP del proyecto**. En el caso de que **se quiera más información sobre que se hizo en cada stash**,al comando anterior se le debe agregar el atributo `--stat` quedando de esta forma `git stash list --stat`.

Para un detalle máximo del stash (cambios en los archivos del stash) se puede utilizar el comando `git stash show id-del-stash`.

`git stash pop`: **Sirve para recuperar los cambios que se encuentran en el stash previamente creado**. Extrae el último stash del stack de stashes, restaura los cambios y luego elimina el stash.

En el caso de que se modifiquen archivos que tengan cambios guardado en el stash, al momento de utilizar `git stash pop` puede que se presente un conflicto, los cuales se resuelven exactamente igual que los conflictos que se presentaban al momento de hacer un merge entre ramas, dependiendo de que se elija, luego de resolver el conflicto quedará el stash con información aún, el cual hay que eliminar utilizando el siguiente comando:

- `git stash drop`: **Se encarga de eliminar el último stash del stack de stashes**. Lo anterior se puede confirmar haciendo un `git stash list`. Si a este comando se le agrega el id de un stash (`git stash drop id-del-stash`) en especifico, se podrá borrar ese stash y no el último ingresado.

Como alternativa a `git stash pop` existe `git stash apply` el cual se encarga de aplicar los cambios que existe en el stash pero no se encarga de eliminar el stash a diferencia de `git stash pop`. 

- `git stash apply id-del-stash`: **Permite aplicar los cambios de un stash en particular**, a diferencia de `git stash pop` que aplica los cambios del último stash ingresado al stack de stash.

Para borras todas las entradas en el stash sin posibilidad de recuperarlas se debe utilizar el comando `git stash clear`.

### Rebase

#### Introducción a los Rebase

- **Rebase (normal):** Sirve para actualizar las ramas. Por ejemplo, en el caso de que hayan dos ramas (Mater y "experimental"), amabas tienen un punto en común desde el cuál nace "experimental", en "experimental" se hacen cambios y todos pero resulta que en Mater igual se hicieron cambios los cuales hacen que desde donde nace "experimental" quede como un punto desactualizado que traerá problemas al momento de hacer un merge, para solucionar lo anterior existe el rebase el cual permite que el punto de inicio de la rama "experimental" se mueva hasta el último commit de la rama Master como si hubiéramos creado la rama en ese punto. Lo anterior se logra haciendo que los commits de la rama "experimental" pasen a un área temporal durante la transición entre el punto de inicio antiguo al nuevo. El comando para hacer lo anterior es `git rebase master`.

- **Rebase interactivo:** `git rebase -i HEAD~n` permite mover n cantidad de commits (no necesariamente desde donde apunta el HEAD) desde donde se indica hacía atrás (o sea que los últimos n commits que se hicieron) a un área temporal los cuales luego serán regresados en el mismo orden que fueron ingresado al área temporal. Esto sirve para: Ordenar commits, corregir mensajes de los commits, unir commits y separar commits.

#### Rebase - Actualizando una rama

Se suele utilizar para evitar tener conflictos al momento de realizar un Merge, de esta forma, toda la información de la rama maestra que puede generar conflicto pasa a estar antes del punto donde se creó la otra rama. 

Antes de realizar un `git rebase rama-en-donde-se-actualizará-el-punto-de-inicio-de-la-otra-rama` se debe asegurar que se está en la rama no principal (usualmente la no *Master*), para esto se utiliza el comando `git brach` y luego `git checkout rama-no-master`. Lo que hace el rebase es mover HEAD al último commit de la rama no master (como si la hubiéramos creado hace poco), cabe destacar que **las ramas aún se encuentran separadas (aunque no lo parezca en la consola)** por lo cual se debe hacer un `git checkout master` (hay que moverse a al rama que se le quiere unir los cambios de la rama no master) y luego un `git merge rama-no-master` (se debe hacer un merge entre la rama en la cual uno se encuentra y la que tiene los cambios). 

#### Rebase - Squash (fusionar commits)

En el caso de tener dos commits similares que perfectamente podrían ser uno sólo, existe el comando `git rebase -i HEAD~n` donde HEAD hace alusión al commit que está siendo apuntado por HEAD y n es la cantidad de commits que se van a seleccionar. Luego de usarlo aparecerá un editor de texto donde se podrá ver los commits seleccionados desde el más viejo al más nuevo. Existen comandos (que se muestran en el editor) donde el importan es *squash* el cual se pone en el último commit al cual se le quiere fusionar los commits que se encuentran sobre él. Luego de lo anterior se deben guardar los cambios presionando *esc* para salir del modo editor (al cual se ingresaba presionando *a*) y luego se teclea *:wq*, lo anterior hace que aparezca otro editor en donde se puede poner el nuevo commit que para la fusión de commits.

#### Rebase - Reword (Actualizar mensaje del commit)

Se utiliza un rebase interactivo en el cual en el n va 1 (haciendo referencia al commit en el cual uno se encuentra y quiere cambiar el nombre), dentro del editor de texto, **no hay que editar directamente el mensaje del commit**, hay que cambiar el *pick* por *reword*, salimos del modo edición, guardamos y salimos para ir al siguiente editor de texto en donde ya podremos editar el mensaje del commit. **En el caso de que salga [detached HEAD hash-del-commit]**, es necesario que hacer un `git checkout master` para asegurar que no se vaya a crear una rama en algún punto. 

#### Rebase - Edit (separar commits)

En el caso de que se quiera separar un commit en varios commit (por ejemplo un commit mal hecho que haga referencia a más de un archivo y se quiera hacer un commit para cada archivo) se deben seguir los siguiente pasos: 

1. Se debe realizar un Rebase interactivo en el cual n será igual 2 `git rebase -i HEAD~2`.

2. En el editor de texto se debe cambiar el pick del commit más nuevo (el que se hizo último) por un edit, luego se sale del modo edición y guardan los cambios.

3. Ahora en la consola se dará la opción de utilizar `git commit --amend` pero lo que se utilizará será `git reset HEAD^` con el fin de revertir los cambios que se realizaron (volver al punto anterior del commit sin que los cambios hechos en los archivos desaparezcan) para así poder hacer nuevos commits de cada archivo. **No asustarse si es que al momento de hacer un `git status` aparece que no nos encontramos en una rama**.

4. Con los commits ya listos, sólo queda utilizar el comando `git rebase --continue` para finalizar y dejar de tener el mensaje de que no nos encontramos en una rama.

## Inicios en GitHub

### Conceptos básicos

Git no maneja el acceso al repositorio, hay que considerar que Git y GitHub son cosas distintas.

- **GitHub:** Es una plataforma de desarrollo colaborativo de software para alojar proyectos. Esta plataforma en su modo gratuito (cuenta gratuita) permite: 

    - Repositorios Ilimitados
    - Páginas HTML, CSS y JS ilimitadas
    - Push, Pull, Clones ilimitados
    - Issues, Wikis, estadísticas ilimitadas
    - Organizaciones ilimitadas
    - Participación gratuita en proyectos privados

Lo anterior es posible siempre y cuando el repositorio sea público, de lo contrario hay que pagar US$7 al mes para hacerlo todo privado.

- **Push y Pull:** Son las acciones de subir los cambios hechos y de descargar los cargos hechos (empujar y jalar) desde la computadora al servidor remoto y desde el servidor remoto a la computadora respectivamente.

- **Git Remote:** Hace referencia al repositorio remoto al cual hay que agregarle el repositorio local seleccionado. Para hacer eso hay que hacer lo siguiente: 

    1. Estando previamente registrado y logueado en GitHub, hay que crear un repositorio para nuestro proyecto, el cual nos dará un link que se debe utilizar en el siguiente paso.

    2. Con el repositorio ya creado y el link copiado, hay que dirigirse al directorio del proyecto qu queremos alojar en GitHub (o si aún no hay proyecto se puede crear un nuevo repositorio, GitHub da un pequeño instructivo de como hacerlo con 6 líneas de comando), en él se abre una terminal en la cual se debe utilizar el siguiente comando `git remote add origin https://link-del-repositorio`, el nombre del repositorio debe ser único en nuestra cuenta y no debe llevar tildes o caracteres especiales. En el comando anterior, *add* hace referencia a agregar un nuevo remote, *origin* es el nombre que se le quiere dar a ese remote (es una buena práctica siempre darle ese nombre al primer remote, es un estándar para hacer referencia al origen), el resto es la dirección del repositorio en GitHub. Cabe destacar que igual se puede hacer por SSH (algunos dicen que es más seguro que HTTPS, pero para más seguridad existe el doble factor que se verá más adelante). **Antes de subir lo que sea, hay que ver que no haya nada en el stage o fuera de él**.

    3. Para saber los remote que existen se utiliza el comando `git remote -v`. Si aparece algo de fetch y otro de push es porque se podría dar el caso que se estén obteniendo datos de un lugar diferente desde donde se hacen los push.

    4. Luego de lo anterior se debe hacer un `git push -u origin master` el cual subirá los archivos del directorio. En el comando, *-u* hace referencia a que la próxima vez que queramos hacer push no sea necesario especificar la rama, *origin* hace referencia al nombre del repositorio remoto en nuestro directorio (el que se dio en el paso 2) y *master* hace referencia a la rama que queremos que se suba al repositorio (en este caso es la rama maestra, podría ser cualquier rama que uno desee).

    5. Una vez hagamos lo anterior, se nos pedirá las credenciales de GitHub para subir los cambios al repositorio. Lo anterior será cada vez que hagamos un push por lo cual se recomienda configurar por defecto las credenciales o conectar con GitHub mediante el uso de SSH.

### Push

Es cuando los cambios realizados se suben al repositorio de GitHub. Hay que ver que no haya nada en el stage o fuera de él. Ya habiéndose hecho el primer `git push -u origin master`, los siguiente push que se hagan no es necesario que lleven el *-u* ni el *master*, ya que como el primer push lleva el -u para que no sea necesario volver a hacer mención a la rama a la cual se le está haciendo push.

Cabe mencionar que al hacer un `git push origin master` no se suben por defectos las etiquetas (tags), por lo cual se deben subir manualmente, ya sea de a 1 o todos a la vez. El comando a utilizar para hacer lo anterior es `git push --tags`.

### Pull 

Es cuando se descargan al directorio local los cambios que se encuentran en el repositorio remoto de GitHub y automáticamente hace un merge (fast-forward). Una buena práctica es que **cada vez que notifiquen cambios o volvamos a trabajar en el código o hayamos hecho un cambio en el código, se recomienda hacer un pull para así mantener actualizado el proyecto de manera local y a su vez identificar futuros conflictos entre cambios realizados**. Para realizar el pull de los cambios se utiliza el comando `git pull origin master` (aunque no es necesario debido a que inicialmente en el primer push se dejo establecida la rama y el repositorio con el *-u* del comando).

### Clonar un repositorio

Se basa en copiar un repositorio ya existente en GitHub en el computador con toda su historia (`git remote -v` nos indicará que ya está conectado al repositorio de GitHub). Para esto se utiliza el comando `git clone link-del-repositorio`. Cabe mencionar que para descargar el repositorio y que el directorio local tenga un nombre indicado por nosotros (no el del directorio del repositorio), se debe utilizar el comando anterior agregando *nombre-indicado* en el comando lo cual deja el comando de la siguiente manera `git clone link-del-repositorio nuevo-nombre`.

### Git Fetch

Descarga los cambios del repositorio remoto sin hacer un merge lo cual puede llegar a ser destructivo dependiendo de la situación. El comando para realizar esto es `git fetch origin master`. En el caso de que existan diferencias, se debe hacer un merge aunque es más rápido hacer un `git pull`.

## GitHub básico

Se recomienda aprender markdown para trabajar de forma más amigable con los archivos .md, además existe markdown aplicado a github que igual se recomienda aprender.

Para buscar un archivo del repositorio dentro de GitHub se puede utilizar la opción *go to file* el cual permite buscar archivos escribiendo algo relacionado a ellos.

### Raw, Blame, History, Edit and Delete

Al entrar a un archivo dentro del repositorio alojado en GitHub, sobre la visualización se encuentra una cierta cantidad de botones que tienen distintas funcionalidades las cuales se proceden a explicar ahora:

- **Raw:** Muestra el archivo crudo, el código tal cual como está escrito, como si fuera salvado en un archivo txt. Cabe mencionar que si se trata de un repositorio público (al parecer da igual si es privado), el link de la visualización en Raw puede ser visualizado por cualquier persona en cualquier navegador.

- **Blame:** Es para saber quién hizo que cambios en el archivo. Los usuarios que hicieron cambios aparecen en la misma línea del cambio que hicieron. Entre el usuario y el código que este modificó, se encuentra un botón el cual nos permite ver el archivo en el estado que se encontraba antes de que el el usuario lo modificará. No hay que asustarse se cuando se vuelve al código faltan archivos, sólo hay que presionar en donde sale el hash del commit y cambiar a master. 

- **History:** Muestra en que commits fue modificado el archivo en cuestión. A la derecha se puede ver el hash corto del commit y un botón *< >* el cuál nos permite ver como se encontraba el repositorio en aquel commit. Al igual que en lo que pasaba con Blame, sólo hay que presionar en el hash y poner *master* para volver al estado actual del repositorio.

- **Edit:** Sirve para modificar los archivos desde GitHub. Luego para guardar la modificación se debe escribir el commit (en la sección commit indicada por la página) y un mensaje (el cual es opcional), se puede hasta crear un rama desde ahí.

- **Delete:** Sirve para borrar el archivo y al igual que *Edit*, pide dejar un commit y se pude crear hasta una rama con ese cambio.

### Creando un archivo en GitHub en una rama aparte

Desde GitHub se pueden crear archivos en una rama nueva (con su correspondiente commit y todo) los cuales para ser unidos (hacer un merge) a la rama maestra se debe hacer un *pull request* (básicamente esto sería **proponer un nuevo archivo**). Si no se añade commit personalizado, GitHub añadirá el que sale en gris en la zona donde se escribe el commit.

Cuando ya se presiona el botón de *propose a new file*, se abre una nueva página que nos dice que abramos una solicitud de pull (*Open a pull request*) en donde se debe rellenar la información pedida antes de presionar el botón *Create a pull request*. Luego de presionado el botón, GitHub se encargará de comparar los cambios y ver si se puede hacer un merge transparente, de lo contrario notificará la existencia de un conflicto el cual hay que solucionar. Ahora sólo queda esperar a que alguien acepte la petición.

Desde el punto de vista de otro usuario del proyecto, en la sección *Pull requests* se mostrarán las peticiones de pull, si uno entra a alguna se verá el mensaje que dejó el otro usuario y el commit, a este último igualmente se puede entrar y ver el o los cambios en el o los archivos, se pueden dejar comentarios (por línea de código o por multiples líneas, que además permiten la sintaxis de markdown), editar el archivo y hasta eliminarlo. Luego de revisar todo se puede elegir que tipo de merge realizar al momento de aceptar el nuevo archivo (o el cambio que se hizo). Post aceptación, GitHub nos da la posibilidad de eliminar la rama donde iba el cambio.

Ya de forma local, se debe realizar el respectivo `git pull origin master` (o un fetch con sus respectivos pasos extras) para mantener el directorio actualizado.

### Creando un archivo en GitHub directamente en la rama maestra

Suponiendo que nos encontramos completamente seguros de que podemos crear un archivo en la rama maestra sin generar algún conflicto con otros archivos, en GitHub se puede crear directamente un archivo en la rama maestra sin necesidad de realizar un pull request, para llevar a cabo lo anterior se debe ir al directorio que alojará el archivo que se creará, luego se debe crear y al momento de hacer el commit, se debe seleccionar la opción que dice *Commit directly to the master branch.* (Commit directamente en la rama maestra), con lo anterior al momento de hacer el commit, el archivo recién creado se creará directamente en el directorio seleccionado sin hacer un pull request o cosas por el estilo.

### Renombrar, borrar y sincronizar el repositorio local

Si en GitHub (en su repositorio local) otro compañero hizo cambios que están sincronizados con el repositorio remoto pero no con el repositorio local en el cual trabajamos, **se recomienda realizar un `git fetch`** en vez de un `git pull`, debido a que de esta manera se **mediante un `git status`** se podrá saber por cuantos commits el repositorio local se encuentrá desactualizado con respecto al repositorio remoto y también sabrás que tipo de merge se puede realizar.

### Comentarios en los commits

Desde GitHub, se pueden dejar comentarios en los commits (da lo mismo en que momento se realizó), uno puede dirigirse a algún commit en especifico y dentro de él ver que se modifico en el archivo y dejar comentarios en las línea de código del archivo que se modificó en el commit. Cabe mencionar que si vamos a la historia del archivo, en los commits donde se hicieron comentarios se podrá ver un símbolo de una burbuja de texto indicando la cantidad de comentarios que hay en ese commit. Recordar que los comentarios aceptan markdown.

## GitHub Avanzado

Los proyectos están compuesto por diferentes integrantes los cuales tienen un ritmo distinto de trabajo el cual puede llegar a causar problemas al momento del desarrollo. Sabiendo lo anterior GitHub ofrece la posibilidad de la creación de flujos de trabajos los cuales permitirán que cada integrante pueda trabajar a su ritmo con el fin de que se genere la menos cantidad de conflictos.

### Fork, Clone y Colaboraciones

**Colaboradores:** Son integrantes que se agregan al repositorio remoto con el fin de que puedan trabajar en el proyecto. Ellos mediante un `git clone` pueden clonar el repositorio en su computadora con el fin de realizar cambios, commits, push y pulls como si fueran el dueño del repositorio.

Cabe mencionar que sin ser colaborador, no se pueden hacer push mediante Git a menos que se haga un Fork con el repositorio.

**Fork:** Al no pertenecer como colaborador a un repositorio al cual se quiere colaborar, se puede realizar un fork el cual se encarga de clonar el repositorio original en la cuenta de GitHub personal **(esto es como si se hubiera creado una rama nueva en el repositorio original)**. Gracias a lo anterior se puede hacer todo como si fuéramos colaboradores pero en la versión clonada del repositorio. Sabiendo lo anterior, ¿Cómo se le hacen llegar los cambios al dueño del repositorio original?. La respuesta a la pregunta anterior son los *Pull request*.

**Pull Request:** Es una petición que se le hace a los dueños de un repositorio para que revisen los cambios hechos por uno con el fin de que estos sean incluidos en el repositorio, aunque si los aceptan, lo más probable es que los dejen en una nueva rama antes de hacerlos parte de la rama maestra.

Con todo lo expuesto anteriormente, ya se puede colaborar en repositorios en los cuales no somos colaboradores, aportando así un granito de arena a proyectos de nuestro interés.

### Cloning y Fork

#### Fork

Para realizar un ***Fork*** se debe hacer lo siguiente: 

1. Se debe ir al repositorio de GitHub al cual se le quiere realizar un Fork.
2. Estando el repositorio, se debe presionar el botón fork el cual creará una copia del repositorio de GitHub en nuestra cuenta personal (puede tomar algo de tiempo). En la página principal de GitHub (cuenta personal) se podrá ver los repositorios que tenemos y el repositorio clonado con *Fork* tendrá un icono distinto.
3. Lo último que se debe hacer es clonar el repositorio creado mediante el uso de *Fork* a la computadora para poder trabajar en él. 

#### Cloning

Para clonar el repositorio hay que utilizar el comando `git clone link-de-clonación nombre-carpeta` (en el comando anterior el nombre-carpeta se reemplaza por el nombre de la carpeta que queremos que tenga el repositorio de forma local. En el caso de que no se quiera cambiar el nombre de la carpeta, quedará el nombre por default que tiene en el repositorio de GitHub).

#### Pull Request

Para hacer un *Pull Request* en un repositorio que previamente se le hizo *Fork*, se debe hacer lo siguiente:

1. Debemos estar posicionados en el directorio local en el cual se clonaron los archivos del repositorio que fue clonado mediante *Fork* en nuestra cuenta.

2. Se debe asegurar que el remote está bien instalado. Para llevar a cabo lo anterior se utiliza el comando `git remote -v`, al utilizar ese comando saldrán los links de GitHub que deberían contener a nuestro usuario y no al usuario propietario del directorio original.

3. Hay que tener en cuenta que los cambios realizados a los archivos deben estar ya en un commit y subidos el repositorio remoto de nuestro usuario (el cual es un clon que se hizo con el *Fork*).

4. En GitHub, se debe refrescar para ver los cambios y si se está satisfecho con ellos se puede hacer un *Pull Request* presionando el botón que dice Pull Request.

5. Luego de presionar el botón, se mostrarán los cambios que se realizaron para revisarlos, si se está conformes con ellos se debe presionar el botón *Create pull request*.

6. Al presionar el botón antes mencionados se nos mostrará una especie de formulario en el cual hay que poner el título del *Pull Request* (un comentario corto y conciso) y se da la opción de escribir un mensaje con más información (recordar que ese mensaje acepta markdown).

7. Con la especie de formulario lista sólo queda presionar el botón *Create pull request*, al presionarlo se nos dirigirá al repositorio original, posicionandonos en la sección de *Pull requests* de ese repositorio y mostrándonos nuestra *Pull Request*.

8. Hay que estar constantemente revisando el *Pull Request* para saber si hay discusiones con respectos a cambios. Lo anterior se hace entrando al *Pull Request* y presionando el botón *View pull request* el cual nos llevará al repositorio original en donde se encuentra todos los comentarios y solicitudes que se le hicieron a nuestro *Pull Request*.

9. En el caso de que se haya realizado algún cambio (en base a modificaciones solicitadas por el autor del repositorio por ejemplo), el *Pull Request* se actualizará automáticamente, mostrando las modificaciones hechas sin necesidad de hacer un nuevo *Pull Request*. (No olvidar que los cambios realizados deben quedar registrados con un commit y luego deben ser subidos al repositorio de nuestra cuenta con un *Push*).

Por parte del encargado del repositorio original, en la pestaña de *Pull Request* verá todos los que hay, puede entrar a uno, aceptarlo total o parcialmente, al igual que puede rechazarlo por completo.

Para aceptarlo parcialmente se hace lo siguiente:

1. Se entra al *Pull Request*.

2. Se revisan los cambios que se hicieron.

3. Se entra al commit del cambio que no se aceptará para comentarlo, para luego solicitar los cambios con el fin de que los autores del cambio sean notificados de los comentarios y solicitudes de cambios que hicieron los encargados del repositorio.

Con los cambios solicitados ya realizados por los autores de los mismos, solo queda aprobar el *Pull Request* y luego hacer un merge (se hace un squash merge en el caso de que se quieran eliminar commits, eso se hace por temas de limpieza).

## Actualizando nuestro Fork

Esto se utiliza cuando no se da acceso directo al repositorio central (original) en donde alguien realiza un *Fork* para trabajar de forma aislada. Lo anterior tiene un problema y es que si otro integrante del proyecto hace cambios en su *Fork* y luego los sube al repositorio principal, nuestro *Fork* queda desactualizado y eso puede provocar futuros conflictos por lo cual ¿Cómo actualizamos nuestro *Fork*?.

1. Se debe agregar un nuevo remote a nuestro repositorio local. Para hacer esto hay que dirigirse al repositorio original (central) para copiar el link de GitHub (como si se tratara de que fuéramos a hacer un *clone*), luego en la terminal del repositorio local, se debe utilizar el comando `git remote add upstream link-del-repositorio` (upstream hace referencia al repositorio central al que le hicimos un *Fork* y al cual no podemos realizar push directos pero necesitamos saber los cambios que se realizan en él para mantener nuestro *Fork* actualizado y no generar conflictos a futuro).

2. Con el nuevo remote (upstream) agregado a nuestro repositorio local, se debe realizar un `git pull upstream master` para hacer el merge a la rama maestra (de todas formas en el caso de que no se sepa que se hizo en el repositorio central, es mejor hacer un `git fetch upstream master` para evitar conflictos y luego realizar un `git pull upstream master` para que se haga el merge entre los cambios del repositorio central y nuestro repositorio local proveniente de un *Fork*). 

3. Ya con el repositorio local actualizado queda realizar un `git push origin master` para actualizar el repositorio clonado con *Fork* que se encuentra en nuestra cuenta de GitHub.

**Los pasos anteriores se deben realizar cada vez que un *Pull Request* haya sido aceptado en el repositorio central (upstream)**.