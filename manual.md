# Documentacion de  Git, Git flow y Github

Es una guia rapida de todo tipos de comando a usar para el uso de gi, git flow y git actions, tendrmeos enlaces de paginas principales donde enriquese la informacion de esta guia. 

- [git](#git)
    - [Configuracion Basica](#configuracion-basica)
    - [conexion con https](#conexion-con-https)
    - [conexion con  llaves](#creacion-de-llaves)
- [Features](#features)
    - [Markdown features](#markdown-features)
    - [Wiki features](#wiki-features)
- [Key Bindings](#key-bindings)
- [GFM Specific Features](#gfm-specific-features)
- [Commands for Command Palette](#commands-for-command-palette)
    - [General Commands](#general-commands)
    - [Links, References and Footnotes](#links-references-and-footnotes)
    - [Folding and Navigation](#folding-and-navigation)
- [Configuration](#configuration)
    - [Additional color themes:](#additional-color-themes)
- [Tips](#tips)
- [Enable WYSIWYG](#enable-wysiwyg)
- [Troubleshooting](#troubleshooting)
    - [Error loading syntax file...](#error-loading-syntax-file)
    - [Roll back to an older version](#roll-back-to-an-older-version)
- [Related Plugins](#related-plugins)
- [Known Bugs](#known-bugs)
- [Contributing](#contributing)
- [Credits](#credits)
- [Donation](#donation)
- [License](#license)

<!-- /MarkdownTOC -->

## Git

miraremos de una forma rapida lo que son las configuraciones basicas,conexion por http o por ssh a tu repositorio remoto y algunos comandos mas usados.

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

### Inicio y conexión de reposiotio locoal y remoto

cuando creamos por primera vez un repositorio tanto local como remoto , lo primero que tendremos que hacer es uvicarnos donde sera guardado el codigo localmente cuando nos indiquemos en la carpeta ideal aremso click derecho y escojeremos la herramiento de basg de git( esot es en windows)

![Figure 1](./images/bashgit.png)

https://git-scm.com/book/es/v2/Personalizaci%C3%B3n-de-Git-Configuraci%C3%B3n-de-Git

