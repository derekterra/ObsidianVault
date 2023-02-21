# **git init:** 
lo usamos para determinar la carpeta en la que vamos a trabajar.

# **git status:** 
lo usamos para saber si tenemos un archivo añadido o borrado en staging area, para saber en la rama en la que estamos y si tenemos commits.

# **git add:** 
es para añadir un archivo a nuestra rama seguidamente ponemos entre comillas el nombre de nuestro archivo o poner un punto para añadir todos los archios de nuestra carpeta.

Puedes agregar archivos individuales: git add archivo.txt
Puedes agregar todos los archivos dentro de la carpeta: git add .

# **git rm:** 
Este comando nos ayuda a eliminar archivos de Git sin eliminar su historial del sistema de versiones. Esto quiere decir que si necesitamos recuperar el archivo solo debemos “viajar en el tiempo” y recuperar el último commit antes de borrar el archivo en cuestión.

Recuerda que `git rm` no puede usarse así nomás. Debemos usar uno de los flags para indicarle a Git cómo eliminar los archivos que ya no necesitamos en la última versión del proyecto:

-   `git rm --cached`: Elimina los archivos de nuestro repositorio local y del área de staging, pero los mantiene en nuestro disco duro. Básicamente le dice a Git que deje de trackear el historial de cambios de estos archivos, por lo que pasaran a un estado `untracked`.
-   `git rm --force`: Elimina los archivos de Git y del disco duro. Git siempre guarda todo, por lo que podemos acceder al registro de la existencia de los archivos, de modo que podremos recuperarlos si es necesario (pero debemos usar comandos más avanzados).

# **git commit:** 
se usa para añadir un commit a nuestra rama, también podemos ponerle un **-am** seguidamente ponemos entre comillas nuestro ensaje.

# **git config:** 
muestra configuraciones de git también podemos usar **–list** para mostrar la configuración por defecto de nuestro git y si añadimos --show-origin _inhales_ nos muestra las configuraciones guardadas y su ubicación.

# **git config --global [user.name](http://user.name/):** 
cambia de manera global el nombre del usuario, seguidamente ponemos entre comillas nuestro nombre.

# **git config --global user.email:** 
cambia de manera global el email del usuario, seguidamente ponemos entre comillas nuestro nombre.

# **git log:** 
se usa para ver la historia de nuestros archivos, los commits, el usuario que lo cambió, cuando se realizaron los cambios etc. seguidamente ponemos el nombre de nuestro archivo.
## git log --stat
Nos muestra los cambios especificos de cada commit desde el mas reciente hasta el mas viejo

NOTA tambien nos muestra el id de cada uno de los commit realizados

## git log --all
Nos muestran todos los cambios que se han realizado

## git log --all --graph
Muestra una vista grafica de los cambios

## git log --all --graph --decorate --oneline
Muestra una vista grafica de los cambios todavia mas completa

# git checkout "IdCommit1" archivo.txt
Volvemos a nuestro archivo a la version del commit indicada, sin cambiar nada en el staging 
Tambien podemos usar . para traer todo
## git checkout master archivo.txt
Volvemos a nuestro archivo a la version que teniamos antes de hacer el primer checkout, sin cambiar nada en el staging
# git reset
Este comando nos ayuda a volver en el tiempo. Pero no como `git checkout` que nos deja ir, mirar, pasear y volver. Con `git reset` volvemos al pasado sin la posibilidad de volver al futuro. Borramos la historia y la debemos sobreescribir. No hay vuelta atrás.

Este comando es **muy peligroso** y debemos emplearlo solo en caso de emergencia. Recuerda que debemos usar alguna de estas dos opciones:
## git reset "IdCommit1" --soft
Volvemos nuestro archivo a la version del commit indicada, pero sin borrar los commits usados anteriormente
No te modifica la carpeta o archivos, solo el repositorio

## git reset "IdCommit1" --hard
Volvemos nuestro archivo a la version del commit indicada, BORRANDO TODOS los commits usados anterioremente a la version del commit indicada

Borra la carpeta
![[Pasted image 20221221230952.png]]

# git show
Nos muestra los cmabios que han existido sobre los dos ultimos commits de un archivo

# git clone
Nos permite clonar repositorios publicos a nuestro equipo local

```
git clone [link http]
```

# git diff
Nos muestra las diferencias entro los cambios que estan en staging y los que aun no se han añadido

## git diff "IdCommit1" "IdCommit2"
Nos muestra las diferencias entre las 2 versiones de los commits

![[Pasted image 20221215202256.png]]



# Funcionamiento de Git
![[Pasted image 20221215205330.png]]

# Grafica visual del funcionamiento de los comandos
![[Pasted image 20230103200658.png]]

# git remote

![[Pasted image 20230103203357.png]]

![[Pasted image 20230122173253.png]]

# Llaves publicas y privadas
Las **llaves públicas y privadas**, conocidas también como cifrado asimétrico de un solo camino, sirven para mandar mensajes privados entre varios nodos con la lógica de que firmas tu mensaje con una llave pública vinculada con una llave privada que puede leer el mensaje.

Las llaves públicas y privadas nos ayudan a cifrar y descifrar nuestros archivos de forma que los podamos compartir sin correr el riesgo de que sean interceptados por personas con malas intenciones.

## Cómo funciona un mensaje cifrado con llaves públicas y privadas

-   1.  Ambas personas deben crear su llave pública y privada.
-   2.  Ambas personas pueden compartir su llave pública a las otras partes (recuerda que esta llave es pública, no hay problema si la “interceptan”).
-   3.  La persona que quiere compartir un mensaje puede usar la llave pública de la otra persona para cifrar los archivos y asegurarse que solo puedan ser descifrados con la llave privada de la persona con la que queremos compartir el mensaje.
-   4.  El mensaje está cifrado y puede ser enviado a la otra persona sin problemas en caso de que los archivos sean interceptados.
-   5.  La persona a la que enviamos el mensaje cifrado puede emplear su llave privada para descifrar el mensaje y ver los archivos.

Nota: puedes compartir tu llave pública, pero nunca tu llave privada.


![[Pasted image 20230122174050.png]]

# Generar llaves
En este ejemplo, aprenderemos **cómo configurar nuestras llaves SSH en local**.

## Cómo generar tus llaves SSH

### 1. Generar tus llaves SSH**

Recuerda que es muy buena idea proteger tu llave privada con una contraseña.

```
ssh-keygen -t rsa -b 4096 -C "tu@email.com"
```

### 2. Terminar de configurar nuestro sistema.

**En Windows y Linux**:

-   Encender el “servidor” de llaves SSH de tu computadora:

```
eval $(ssh-agent -s)
```

-   Añadir tu llave SSH a este “servidor”:

```
ssh-add ruta-donde-guardaste-tu-llave-privada
```

# Conexion a Github con SSH
La creación de las SSH es necesario solo una vez por cada computadora. Aquí conocerás **cómo conectar a GitHub usando SSH**.

Luego de crear nuestras llaves SSH podemos entregarle la llave pública a GitHub para comunicarnos de forma segura y sin necesidad de escribir nuestro usuario y contraseña todo el tiempo.

Para esto debes entrar a la [Configuración de Llaves SSH en GitHub](https://github.com/settings/keys), crear una nueva llave con el nombre que le quieras dar y el contenido de la llave pública de tu computadora.

Ahora podemos actualizar la URL que guardamos en nuestro repositorio remoto, solo que, en vez de guardar la URL con HTTPS, vamos a usar la URL con SSH:

```
ssh
git remote set-url origin url-ssh-del-repositorio-en-github
```

## Comandos para copiar la llave SSH:

-   **Windows (Git Bash)**:

```
clip < ~/.ssh/id_rsa.pub
```

# Tags y versiones en Git y GitHub

Los tags o etiquetas nos permiten asignar versiones a los commits con cambios más importantes o significativos de nuestro proyecto.

## Comandos para trabajar con etiquetas:

-   Crear un nuevo tag y asignarlo a un commit: **`git tag -a nombre-del-tag id-del-commit`**.
-   Borrar un tag en el repositorio local: **`git tag -d nombre-del-tag`**.
-   Listar los tags de nuestro repositorio local: **`git tag`** o **`git show-ref --tags`**.
-   Publicar un tag en el repositorio remoto: **`git push origin --tags`**.
-   Borrar un tag del repositorio remoto: `git tag -d nombre-del-tag` y **`git push origin :refs/tags/nombre-del-tag`**.

Para generar un comando complejo con varios comandos de una forma optimizada, utilizamos conjuntos de sentencias conocidas como _alias_.

# Ver historial de cambios de manera grafica

Existen dos maneras:
```
git config alias.arbolito "log --all --graph --decorate --oneline"
```

y 
```
gitk
```

## Cómo aregar un alias solo para git

-   Para un proyecto:

```
git config alias.arbolito "log --all --graph --decorate --oneline"
```

-   Global:

```
git config --global alias.arbolito "log --all --graph --decorate --oneline"
```

-   Para correrlo:

```
git arbolito
```



# Pull request:

Es una funcionalidad de github (en gitlab llamada merge request y en bitbucket push request), en la que un colaborador pide que revisen sus cambios antes de hacer merge a una rama, normalmente master.

Al hacer un pull request se genera una conversación que pueden seguir los demás usuarios del repositorio, así como autorizar y rechazar los cambios.

El flujo del pull request es el siguiente

1.  Se trabaja en una **rama paralela** los cambios que se desean (`git checkout -b <rama>`)
2.  Se hace un **commit** a la rama (`git commit -am '<Comentario>'`)
3.  Se **suben** al **remoto** los **cambios** (`git push origin <rama>`)
4.  En GitHub se hace el `pull request` comparando la **rama master** con la rama del **fix**.
5.  Uno, o varios colaboradores revisan que el **código sea correcto** y dan **feedback** (en el chat del pull request)
6.  El colaborador hace los cambios que desea en la **rama** y lo **vuelve a subir** al remoto (automáticamente jala la historia de los cambios que se hagan en la rama, en remoto)
7.  Se **aceptan los cambios** en GitHub
8.  Se hace **merge** a `master` desde GitHub

**Importante**: Cuando se modifica una `rama`, también se modifica el `pull request`.


# Forks o Bifurcaciones

Es una característica única de GitHub en la que se crea una copia exacta del estado actual de un repositorio directamente en GitHub, éste repositorio podrá servir como otro origen y se podrá clonar (como cualquier otro repositorio), en pocas palabras, lo podremos utilizar como un git cualquiera  
.  
Un fork es como una bifurcación del repositorio completo, tiene una historia en común, pero de repente se bifurca y pueden variar los cambios, ya que ambos proyectos podrán ser modificados en paralelo y para estar al día un colaborador tendrá que estar actualizando su fork con la información del original.  
.  
Al hacer un fork de un poryecto en GitHub, te conviertes en dueñ@ del repositorio fork, puedes trabajar en éste con todos los permisos, pero es un repositorio completamente diferente que el original, teniendo alguna historia en común.  
.  
Los forks son importantes porque es la manera en la que funciona el open source, ya que, una persona puede no ser colaborador de un proyecto, pero puede contribuír al mismo, haciendo mejor software que pueda ser utilizado por cualquiera.  
.  
Al hacer un fork, GitHub sabe que se hizo el fork del proyecto, por lo que se le permite al colaborador hacer pull request desde su repositorio propio.

## Trabajando con más de 1 repositorio remoto

Cuando trabajas en un proyecto que existe en **diferentes repositorios remotos** (normalmente a causa de un **fork**) es muy probable que desees poder **trabajar con ambos repositorios**, para ésto puedes crear un **remoto adicional** desde consola.

```bash
git remote add <nombre_del_remoto> <url_del_remoto> 
```

```bash
git remote upstream https://github.com/freddier/hyperblog
```

Al crear un **remoto adicional** podremos, hacer **pull** desde el nuevo **origen** (en caso de tener permisos podremos hacer fetch y push)

```bash
git pull <remoto> <rama>
```

```bash
git pull upstream master
```

Éste `pull` nos traerá los **cambios del remoto**, por lo que se estará al día en el proyecto, el flujo de trabajo cambia, en adelante se estará trabajando haciendo **pull desde el upstream** y **push al origin** para pasar a hacer **pull request**.

```bash
git pull upstream master
git push origin master
```

# Ignorar archivos en el repositorio con .gitignore
No todos los archivos que agregas a un proyecto deberían ir a un repositorio. Por ejemplo, cuando tienes un archivo donde están tus contraseñas que comúnmente tienen la extensión `.env` o cuando te estás conectando a una base de datos; **son archivos que nadie debe ver**.

Por diversas razones, no todos los archivos que agregas a un proyecto deberían guardarse en un repositorio. Esto es porque hay archivos que no todo el mundo debería de ver, y hay archivos que al estar en el repositorio ralentizan el proceso de desarrollo (por ejemplo: los binary large objects, blob, que tardan en descargarse).

Para que no se suban estos archivos no deseados se puede crear un archivo con el nombre .gitignore en la raíz del repositorio con las reglas para los archivos que no se deberían subir: Aquí puedes ver la [sintaxis de los .gitignore](https://git-scm.com/docs/gitignore).

Las razones principales para tomar la decisión de no agregar un archivo a un repositorio son:

-   Es un archivo con contraseñas (normalmente con la extensión .env)
-   Es un blob (binary large object, objeto binario grande), mismos que son difíciles de gestionar en git.
-   Son archivos que se generan corriendo comandos, por ejemplo la carpeta node_modules, que genera **npm** al correr el comando npm install
# Readme.md es una excelente práctica

`README.md` es el lugar donde se explica de qué trata el proyecto, cómo utilizarlo y demás información que se considere que se deba conocer cualquier persona que vaya a trabajar de alguna forma con el proyecto.  
.  
Los archivos README son escritos en un lenguaje llamado **markdown**, por eso la extensión .md, mismo que es un estándar de escritura en diversos sitios (como Platzi, Wikipedia y el mismo GitHub). Aquí puedes ver las [reglas de markdown](https://www.markdownguide.org/extended-syntax).

Los [README.md](http://readme.md/) pueden estar en todas las carpetas, pero el más importante es el que se encuentra en la raíz. Este documento ayuda a que los colaboradores sepan información relevante del proyecto, módulo o sección. Puedes crear cualquier archivo con la extensión .md pero solo los [README.md](http://readme.md/) los mostrará por defecto GitHub.

# Tu sitio web público con GitHub Pages

GitHub tiene un servicio de hosting gratis llamado **GitHub Pages**. Con él, puedes tener un repositorio alojado en GitHub y hacer que el contenido se muestre en la web en tiempo real.

Este es un sitio para nuestros proyectos donde lo único que tenemos que hacer es tener un repositorio alojado. En la página, podemos seguir las instrucciones para crear este repositorio

## Pasos para subir un repositorio a GitHub Pages

-   Debemos tomar la llave SSH y hacer un `git clone #SSHexample` en mi computador local (Home).
-   Luego, accederemos a la carpeta nueva que aparece en nuestra máquina local.
-   Creamos un nuevo archivo que se llame index.html
-   Guardamos los cambios, hacemos un `git pull` y seguido de esto un `git push` a `master`.
-   Vamos a las opciones de _settings_ de este repositorio y, en la parte de abajo, en la columna Github Pages, configuramos el _source_ o fuente para que traiga la rama _master_
-   Guardamos los cambios.

Después de esto, podremos ver nuestro trabajo en la web como si tuviéramos nuestro propio servidor.

# Git Rebase: reorganizando el trabajo realizado
Rebase es el proceso de mover o combinar una secuencia de confirmaciones en una nueva confirmación base. La reorganización es muy útil y se visualiza fácilmente en el contexto de un flujo de trabajo de [ramas de funciones](https://platzi.com/clases/1557-git-github/19947-que-es-un-branch-rama-y-como-funciona-un-merge-en-/). El proceso general se puede visualizar de la siguiente manera.

![rebase1.png](https://static.platzi.com/media/user_upload/rebase1-45694a4e-3411-4785-8d6a-1545057ee1fc.jpg)

Para hacer un rebase en la rama feature de la rama master, correrías los siguientes comandos:

```
git checkout feature
git rebase master
```

Esto _trasplanta_ la rama feature desde su locación actual hacia la punta de la rama master:

![rebase2.png](https://static.platzi.com/media/user_upload/rebase2-3bcb1804-1167-4d2f-af90-c7fed7a7fd6c.jpg)

Ahora, falta fusionar la rama feature con la rama master

```
git checkout master
git rebase feature
# No reorganices el historial público
```

Nunca debes reorganizar las confirmaciones una vez que se hayan enviado a un repositorio público. La reorganización sustituiría las confirmaciones antiguas por las nuevas y parecería que esa parte del historial de tu proyecto se hubiera desvanecido de repente.

El comando **_rebase_** es **_una mala práctica, sobre todo en repositorios remotos. Se debe evitar su uso, pero para efectos de práctica te lo vamos a mostrar, para que hagas tus propios experimentos. Con `rebase` puedes recoger todos los cambios confirmados en una rama y ponerlos sobre otra. (primero se le hace rebase a la rama experiment y luego rebase al master, si no corre el riesgo de tener conflictos)

```bash
# Cambiamos a la rama que queremos traer los cambios
git checkout experiment
# Aplicamos rebase para traer los cambios de la rama que queremos 
git rebase master
```



# Git Stash: Guardar cambios en memoria y recuperarlos después
El _stashed_ nos sirve para guardar cambios para después, Es una lista de estados que nos guarda algunos cambios que hicimos en Staging para poder cambiar de [rama o branch](https://platzi.com/clases/1557-git-github/19947-que-es-un-branch-rama-y-como-funciona-un-merge-en-/) sin perder el trabajo que todavía no guardamos en un commit

Ésto es especialmente útil porque hay veces que no se permite cambiar de rama, ésto porque tenemos cambios sin guardar, no siempre es un cambio lo suficientemente bueno como para hacer un commit, pero no queremos perder ese código en el que estuvimos trabajando.

El stashed nos permite cambiar de ramas, hacer cambios, trabajar en otras cosas y, más adelante, retomar el trabajo con los archivos que teníamos en Staging, pero que podemos recuperar, ya que los guardamos en el Stash.

## git stash

El comando git stash guarda el trabajo actual del Staging en una lista diseñada para ser temporal llamada Stash, para que pueda ser recuperado en el futuro.

Para agregar los cambios al stash se utiliza el comando:

```
git stash

```

Podemos poner un mensaje en el stash, para asi diferenciarlos en git stash list por si tenemos varios elementos en el stash. Ésto con:

```
git stash save "mensaje identificador del elemento del stashed"

```

## Obtener elelmentos del stash

El stashed se comporta como una [Stack](https://es.wikipedia.org/wiki/Pila_(inform%C3%A1tica)) de datos comportándose de manera tipo [LIFO](https://es.wikipedia.org/wiki/LIFO) (del inglés _Last In, First Out_, «último en entrar, primero en salir»), así podemos acceder al método pop.

El método **pop** recuperará y sacará de la lista el **último estado del stashed** y lo insertará en el **staging area**, por lo que es importante saber en qué _branch_ te encuentras para poder recuperarlo, ya que el stash será **agnóstico a la rama o estado en el que te encuentres**. Siempre recuperará los cambios que hiciste en el lugar que lo llamas.

Para recuperar los últimos cambios desde el stash a tu staging area utiliza el comando:

```
git stash pop

```

Para aplicar los cambios de un stash específico y eliminarlo del stash:

```
git stash pop stash@{<num_stash>}

```

Para retomar los cambios de una posición específica del Stash puedes utilizar el comando:

```
git stash apply stash@{<num_stash>}

```

Donde el `<num_stash>` lo obtienes desden el `git stash list`

## Listado de elementos en el stash

Para ver la lista de cambios guardados en Stash y así poder recuperarlos o hacer algo con ellos podemos utilizar el comando:

```
git stash list

```

Retomar los cambios de una posición específica del Stash || Aplica los cambios de un stash específico

## Crear una rama con el stash

Para crear una rama y aplicar el stash más reciente podemos utilizar el comando

```
git stash branch <nombre_de_la_rama>

```

Si deseas crear una rama y aplicar un stash específico (obtenido desde `git stash list`) puedes utilizar el comando:

```
git stash branch nombre_de_rama stash@{<num_stash>}

```

Al utilizar estos comandos **crearás una rama** con el nombre `<nombre_de_la_rama>`, te pasarás a ella y tendrás el **stash especificado** en tu **staging area**.

## Eliminar elementos del stash

Para eliminar los cambios más recientes dentro del stash (el elemento 0), podemos utilizar el comando:

```
git stash drop

```

Pero si, en cambio, conoces el `índice` del stash que quieres borrar (mediante `git stash list`) puedes utilizar el comando:

```
git stash drop stash@{<num_stash>}

```

Donde el `<num_stash>` es el `índice` del cambio guardado.

Si, en cambio, deseas eliminar todos los elementos del stash, puedes utilizar:

```
git stash clear

```

## Consideraciones:

-   El cambio más reciente (al crear un stash) **SIEMPRE** recibe el valor 0 y los que estaban antes aumentan su valor.
-   Al crear un stash tomará los archivos que han sido modificados y eliminados. Para que tome un archivo creado es necesario agregarlo al Staging Area con git add [nombre_archivo] con la intención de que git tenga un seguimiento de ese archivo, o también utilizando el comando git stash -u (que guardará en el stash los archivos que no estén en el staging).
-   Al aplicar un stash este no se elimina, es buena práctica eliminarlo.


# Git Clean: limpiar tu proyecto de archivos no deseados

Mientras estamos trabajando en un repositorio podemos añadir archivos a él, que realmente no forma parte de nuestro directorio de trabajo, archivos que no se deberían de agregar al repositorio remoto.

El comando `clean` actúa en archivos sin seguimiento, este tipo de archivos son aquellos que se encuentran en el directorio de trabajo, pero que aún no se han añadido al índice de seguimiento de repositorio con el comando `add`.

```
$ git clean

```

La ejecución del comando predeterminado puede producir un error. La configuración global de Git obliga a usar la opción `force` con el comando para que sea efectivo. Se trata de un importante mecanismo de seguridad ya que este comando no se puede deshacer.

## Revisar que archivos no tienen seguimiento.

```
$ git clean --dry-run

```

## Eliminar los archivos listados de no seguimiento.

```
$ git clean -f
```

Git clean tiene muchísimas opciones adicionales, que puedes explorar al ver su [documentación oficial](https://git-scm.com/docs/git-clean).

# Git cherry-pick: traer commits viejos al head de un branch

**Git Cherry-pick** es un comando que permite tomar uno o varios commits de otra rama o [branch](https://platzi.com/clases/1557-git-github/19947-que-es-un-branch-rama-y-como-funciona-un-merge-en-/) sin tener que hacer un merge completo. Así, gracias a cherry-pick, podríamos aplicar los commits relacionados con nuestra funcionalidad en la rama master sin necesidad de hacer un merge.

Para demostrar cómo utilizar git cherry-pick, supongamos que tenemos un repositorio con el siguiente estado de rama:

```
a -b - c - d   Master
         \
           e - f - g Feature

```

El uso de git cherry-pick es sencillo y se puede ejecutar de la siguiente manera:

```
git checkoutmaster
```

En este ejemplo, commitSha es una referencia de confirmación. Puedes encontrar una referencia de confirmación utilizando el comando git log. En este caso, imaginemos que queremos utilizar la confirmación ‘f’ en la rama master. Para ello, primero debemos asegurarnos de que estamos trabajando con esa rama master.

```
git cherry-pick f

```

Una vez ejecutado, el historial de Git se verá así:

```
a -b - c - d - f   Master
         \
           e - f - g Feature

```

La confirmación f se ha sido introducido con éxito en la rama de funcionalidad

## Atención

Cherry-pick **es una mala práctica** porque significa que estamos reconstruyendo la historia, **usa cherry-pick con sabiduría**. Si no sabes lo que estás haciendo, mejor evita emplear este comando.

# Git Reset y Reflog: úsese en caso de emergencia


Git guarda todos los cambios aunque decidas borrarlos, al borrar un cambio lo que estás haciendo sólo es actualizar la punta del branch, para gestionar éstas puntas existe un mecanismo llamado registros de referencia o `reflogs`…La gestión de estos cambios es mediante los hash’es de referencia (o `ref`) que son apuntadores a los commits…Los recoges registran cuándo se actualizaron las referencias de Git en el repositorio local (sólo en el local), por lo que si deseas ver cómo has modificado la historia puedes utilizar el comando:

```
git reflog

```

Muchos comandos de Git aceptan un parámetro para especificar una referencia o “ref”, que es un puntero a una confirmación sobre todo los comandos:

-   `git checkout` Puedes moverte sin realizar ningún cambio al commit exacto de la `ref`
    
    ```
    git checkout eff544f
    
    ```
    
-   `git reset`: Hará que el último commit sea el pasado por la `ref`, usar este comando sólo si sabes exactamente qué estás haciendo
    
    ```
    git reset --hard eff544f # Perderá todo lo que se encuentra en staging y en el Working directory y se moverá el head al commit eff544f
    git reset --soft eff544f # Te recuperará todos los cambios que tengas diferentes al commit eff544f, los agregará al staging area y moverá el head al commit eff544f
    
    ```
    
-   `git merge`: Puedes hacer merge de un commit en específico, funciona igual que con una branch, pero te hace el merge del estado específico del commit mandado
    
    ```
    git checkout master
    git merge eff544f # Fusionará en un nuevo commit la historia de master con el momento específico en el que vive
    ```
    

¿Qué pasa cuando todo se rompe y no sabemos qué está pasando? Con `git reset HashDelHEAD` nos devolveremos al estado en que el proyecto funcionaba.

-   `git reset --soft HashDelHEAD` te mantiene lo que tengas en staging ahí.
-   `git reset --hard HashDelHEAD` resetea absolutamente todo incluyendo lo que tengas en staging.

## Atención

`git reset` es una mala práctica, **no deberías usarlo en ningún momento**. Debe ser nuestro último recurso.

# Reconstruir commits en Git con amend


_Remendar_ un commit con `amend` puede modificar el commit más reciente (enmendar) en la misma [rama](https://platzi.com/clases/1557-git-github/19947-que-es-un-branch-rama-y-como-funciona-un-merge-en-/). Lo ejecutamos así:

```
git add -A # Para hacer uso de amend los archivos deben de estar en staging
git commit --amend # Remendar último commit

```

Este comando sirve para agregar archivos nuevos o actualizar el commit anterior y no generar commits innecesarios. También es una forma sencilla de **editar o agregar comentarios al commit anterior** porque abrirá la consola para editar este commit anterior.

## **Atención**

Usar `amend` es una **mala práctica**, sobre todo cuando ya se ha hecho **push o pull** al repositorio remoto. Al momento de hacer amend con algún `commit` que esté en remoto, va a generar un **conflicto** que se va a arreglar haciendo un `commit adicional` y se **perderá el beneficio** del amend.

# Buscar en archivos y commits de Git con Grep y log

A medida que nuestro proyecto en Git se hace más grande, vamos a querer buscar ciertas cosas.

Por ejemplo: ¿cuántas veces en nuestro proyecto utilizamos la palabra _color_?

Para buscar, empleamos el comando `git grep color` y nos buscará en todo el proyecto los archivos en donde está la palabra _color_.

-   Con `git grep -n color` nos saldrá un output el cual nos dirá en qué línea está lo que estamos buscando.
-   Con `git grep -c color` nos saldrá un output el cual nos dirá cuántas veces se repite esa palabra y en qué archivo.
-   Si queremos buscar cuántas veces utilizamos un atributo de HTML lo hacemos con `git grep -c "<p>"`.
```
git grep color -->use la palabra color  
git grep la --> donde use la palabra la  
git grep -n color–> en que lineas use la palabra color  
git grep -n platzi --> en que lineas use la palabra platzi  
git grep -c la --> cuantas veces use la palabra la  
git grep -c paltzi --> cuantas veces use la palabra platzi  
git grep -c “<p>”–> cuantas veces use la etiqueta <p>

git log-S “cabecera” --> cuantas veces use la palabra cabecera en  
todos los commits.

grep–> para los archivos  
log --> para los commits.
```
# Comandos y recursos colaborativos en Git y GitHub

A continuación veremos una lista de comandos colaborativos para facilitar el trabajo remoto en GitHub:

-   `git shortlog -sn`: muestra cuantos commit han hecho cada miembro del equipo.
-   `git shortlog -sn --all`: muestra cuantos commit han hecho cada miembro del equipo, hasta los que han sido eliminados.
-   `git shortlog -sn --all --no-merge`: muestra cuantos commit ha hecho cada miembro, quitando los eliminados sin los merges.
-   `git blame ARCHIVO`: muestra quien hizo cada cosa línea por línea.
-   `git COMANDO --help`:muestra como funciona el comando.
-   `git blame ARCHIVO -Llinea_inicial,linea_final`: muestra quien hizo cada cosa línea por línea, indicándole desde qué línea ver. Ejemplo -L35,50.
-   `git branch -r`: se muestran todas las ramas remotas.
-   `git branch -a`: se muestran todas las ramas, tanto locales como remotas.