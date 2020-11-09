# Documentación de Git, Git Flow y GitHub

Es una guía rapida de todotipo de comandos a usar para el uso de git, git flow y git actions, tendremos enlaces de paginas principales donde enriquece la información de esta guía. 

  - [Git](#git)
    - [Configuración de Git](#configuración-de-git)
    - [Inicio y conexión de reposiotio locoal y remoto](#inicio-y-conexión-de-reposiotio-locoal-y-remoto)
    - [Creando Repositorio en GitHub](#creando-repositorio-en-github)
    - [Creando llaves y agregandola ah github](#creando-llaves-y-agregandola-ah-github)
    - [Conexion ha github por medio de https](#conexion-ha-github-por-medio-de-https)
  - [enlaces](#enlaces)

## Git

miraremos de una forma rapida lo que son las configuraciones básicas, conexión por http o por ssh a tu repositorio remoto y algunos comandos más usados.

***

### Configuración de Git

Con estas operaciones, será fácil conseguir que Git trabaje exactamente como tú, tu empresa o tu grupo.

Podemos acceder a los ajustes de configuración de Git a través del comando git config. Una de las primeras acciones que has realizado con Git ha sido el configurar tu nombre y tu dirección de correo electrónico.

```bash
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```

__core.editor__

Por defecto, Git utiliza cualquier editor que hayas configurado como editor de texto por defecto de tu sistema **( $VISUAL  o  $EDITOR)**. O, si no lo has configurado, utilizará vi como editor para crear y editar las etiquetas y mensajes de tus confirmaciones de cambio (commit). Para cambiar ese comportamiento, puedes utilizar el ajuste core.editor:

```bash
$ git config --global core.editor emacs
```

Para conocer lo que tienes guardado en el archivo de configuracion tan solo tienes que poner 

```bash
$ git config --list
```
o solo inidicar lo que quieres ver como por ejemplo si realmente pusiste el nombre bien o ver si quieres cambiarlo despues.

```bash 
$ git config --global user.name
```
***

### Inicio y conexión de reposiotio locoal y remoto

cuando creamos por primera vez un repositorio tanto local como remoto, lo primero que tendremos que hacer es uvicarnos donde sera guardado el codigo localmente cuando nos indiquemos en la carpeta ideal aremso click derecho y escojeremos la herramiento de base de git(esto es en Windows)

![Figure 1](./assets/bashGit.png)


Después adentro del programa de comando por terminal (Git bash) pondremos git init dándole inicio al repositorio del proyecto 

```bash
$ git init
```
la hacer esto ya podremos ya sea trabajar o terminar la conexión a nuestro repositorio remoto.
>  _Pero antes tenemos que tener echo el repositorio remoto ([creaundo repositorio en github](#creando-repositorio-en-github))  y saber de cual forma conectarnos a nuestro repositorio ya sea por conexión por llaves ([reando llaves y agregandola ah github](#creando-llaves-y-agregandola-ah-github)) o por https([Conexion ha github por medio de https](#conexion-ha-github-por-medio-de-https))_

Después de hacer cambios al proyecto hay que subirlos en versión, Tu repositorio local está compuesto por tres "árboles" administrados por git. El primero es tu Directorio de trabajo que contiene los archivos, el segundo es el Index que actúa como una zona intermedia, y el último es el HEAD que apunta al último commit realizado, para eso usaremos el subcomando add el cual podemos indicar un solo documento o más nombrándolo o solamente indiciándolo con un punto.

  - un solo documento, carpeta etc. (modificación, creación o eliminación)
    ```bash
      $ git add README.md
    ```
  - todas las modificaciones creaciones y eliminaciones del proyecto
    ```bash
    $ git add .
    ``` 
al haber echo eso todo los cambios estarán en la rama index del proyecto
****

### Creando Repositorio en GitHub
 son simples pasos visuales el cual tamibne viene como hacerlo en tu computadora, aun asi se explica.
![Figure 2](./assets/crearRepo.gif)

****
### Creando llaves y agregandola ah github


****
### Conexion ha github por medio de https


****

### Listado Comandos Git
## Configuración Básica

Configurar Nombre que salen en los commits
```ssh
	git config --global user.name "dasdo"
```
Configurar Email
```ssh	
	git config --global user.email dasdo1@gmail.com
```
Marco de colores para los comando
```ssh
	git config --global color.ui true
```

## Iniciando repositorio

Iniciamos GIT en la carpeta donde esta el proyecto
```ssh
	git init
```
Clonamos el repositorio de github o bitbucket
```ssh
	git clone <url>
```
Añadimos todos los archivos para el commit
```ssh
	git add .
```
Hacemos el primer commit
```ssh
	git commit -m "Texto que identifique por que se hizo el commit"
```
subimos al repositorio
```ssh
	git push origin master
```

## GIT CLONE


Clonamos el repositorio de github o bitbucket
```ssh
	git clone <url>
```
Clonamos el repositorio de github o bitbucket ?????
```ssh
	git clone <url> git-demo
```

## GIT ADD


Añadimos todos los archivos para el commit
```ssh
	git add .
```
Añadimos el archivo para el commit
```ssh
	git add <archivo>
```
Añadimos todos los archivos para el commit omitiendo los nuevos
```ssh
	git add --all 
```
Añadimos todos los archivos con la extensión especificada
```ssh
	git add *.txt
```
Añadimos todos los archivos dentro de un directorio y de una extensión especifica
```ssh
	git add docs/*.txt
```
Añadimos todos los archivos dentro de un directorios
```ssh
	git add docs/
```
## GIT COMMIT

Cargar en el HEAD los cambios realizados
```ssh
	git commit -m "Texto que identifique por que se hizo el commit"
```
Agregar y Cargar en el HEAD los cambios realizados
```ssh
	git commit -a -m "Texto que identifique por que se hizo el commit"
```
De haber conflictos los muestra
```ssh
	git commit -a 
```
Agregar al ultimo commit, este no se muestra como un nuevo commit en los logs. Se puede especificar un nuevo mensaje
```ssh
	git commit --amend -m "Texto que identifique por que se hizo el commit"
```
## GIT PUSH

Subimos al repositorio
```ssh
	git push <origien> <branch>
```
Subimos un tag
```ssh
	git push --tags
```
## GIT LOG

Muestra los logs de los commits
```ssh
	git log
```
Muestras los cambios en los commits
```ssh
	git log --oneline --stat
```
Muestra graficos de los commits
```ssh
	git log --oneline --graph
```
## GIT DIFF

Muestra los cambios realizados a un archivo
```ssh
	git diff
	git diff --staged
```
## GIT HEAD

Saca un archivo del commit
```ssh
	git reset HEAD <archivo>
```
Devuelve el ultimo commit que se hizo y pone los cambios en staging
```ssh
	git reset --soft HEAD^
```
Devuelve el ultimo commit y todos los cambios
```ssh
	git reset --hard HEAD^
```
Devuelve los 2 ultimo commit y todos los cambios
```ssh
	git reset --hard HEAD^^
```
Rollback merge/commit
```ssh
	git log
	git reset --hard <commit_sha>
```
## GIT REMOTE

Agregar repositorio remoto
```ssh
	git remote add origin <url>
```
Cambiar de remote
```ssh
	git remote set-url origin <url>
```
Remover repositorio
```ssh
	git remote rm <name/origin>
```
Muestra lista repositorios
```ssh
	git remote -v
```
Muestra los branches remotos
```ssh	
	git remote show origin
```
Limpiar todos los branches eliminados
```ssh
	git remote prune origin 
```
## GIT BRANCH

Crea un branch
```ssh
	git branch <nameBranch>
```
Lista los branches
```ssh
	git branch
```
Comando -d elimina el branch y lo une al master
```ssh
	git branch -d <nameBranch>
```
Elimina sin preguntar
```ssh
	git branch -D <nameBranch>
```
## GIT TAG

Muestra una lista de todos los tags
```ssh
	git tag
```
Crea un nuevo tags
```ssh
	git tag -a <verison> - m "esta es la versión x"
```
## GIT REBASE

Los rebase se usan cuando trabajamos con branches esto hace que los branches se pongan al día con el master sin afectar al mismo

Une el branch actual con el mastar, esto no se puede ver como un merge
```ssh
	git rebase
```
Cuando se produce un conflicto no das las siguientes opciones:

cuando resolvemos los conflictos --continue continua la secuencia del rebase donde se pauso
```ssh	
	git rebase --continue 
```
Omite el conflicto y sigue su camino
```ssh
	git rebase --skip
```
Devuelve todo al principio del rebase
```ssh
	git reabse --abort
```
Para hacer un rebase a un branch en especifico
```ssh	
	git rebase <nameBranch>
```
## OTROS COMANDOS

Lista un estado actual del repositorio con lista de archivos modificados o agregados
```ssh
	git status
```
Quita del HEAD un archivo y le pone el estado de no trabajado
```ssh
	git checkout -- <file>
```
Crea un branch en base a uno online
```ssh
	git checkout -b newlocalbranchname origin/branch-name
```
Busca los cambios nuevos y actualiza el repositorio
```ssh
	git pull origin <nameBranch>
```
Cambiar de branch
```ssh
	git checkout <nameBranch/tagname>
```
Une el branch actual con el especificado
```ssh
	git merge <nameBranch>
```
Verifica cambios en el repositorio online con el local
```ssh
	git fetch
```
Borrar un archivo del repositorio
```ssh
	git rm <archivo> 
```

## Fork

Descargar remote de un fork
```
	git remote add upstream <url>
```

Merge con master de un fork
```
	git fetch upstream
	git merge upstream/master
```
****

### Enlaces
[configuracion git](https://git-scm.com/book/es/v2/Personalizaci%C3%B3n-de-Git-Configuraci%C3%B3n-de-Git)

