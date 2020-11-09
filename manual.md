# Documentación de Git, Git Flow y GitHub

Es una guía rapida de todotipo de comandos a usar para el uso de git, git flow y git actions, tendremos enlaces de paginas principales donde enriquece la información de esta guía. 

- [Documentación de Git, Git Flow y GitHub](#documentación-de-git-git-flow-y-github)
  - [Git](#git)
    - [Configuración de Git](#configuración-de-git)
    - [Inicio y conexión de reposiotio locoal y remoto](#inicio-y-conexión-de-reposiotio-locoal-y-remoto)
    - [Creando Repositorio en GitHub](#creando-repositorio-en-github)
    - [Creando llaves y agregandola ah github](#creando-llaves-y-agregandola-ah-github)
    - [Conexion ha github por medio de https](#conexion-ha-github-por-medio-de-https)


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
la hacer esto ya podremos ya sea trabajar o terminar la conexión a nuestro repositorio remoto. Pero antes tenemos que tener echo el repositorio remoto (liga)  y saber de cual forma conectarnos a nuestro repositorio ya sea por conexión por llaves (liga) o por https(liga)

****

### Creando Repositorio en GitHub


****
### Creando llaves y agregandola ah github

****
### Conexion ha github por medio de https

****

https://git-scm.com/book/es/v2/Personalizaci%C3%B3n-de-Git-Configuraci%C3%B3n-de-Git

