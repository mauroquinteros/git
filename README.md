# Introducción a Git y GitHub

Este repositorio es un resumen del [curso de Git y Github](https://platzi.com/cursos/git-github/) en Platzi 💚

Si deseas aportar a este repositorio puedes hacer un pull request una vez hayas terminado de leer este resumen.

 1. [Cómo funciona Git](#1-cómo-funciona-git)

  - [Instalación](#instalación-de-git)
  - [Configuración](#configuración-de-git)
  - [Beneficios](#beneficios-de-git)
 2. [Áreas de trabajo de Git](#2-áreas-de-trabajo-de-git)
 3. Los estados de un archivo
 4. Flujo básico de trabajo de git
 5. Comandos Básicos de git
 6. Manejo de ramas (branch) en Git
 7. Flujo de trabajo profesional usando Github
 8. Manejo de los pull requests y forks

## 1. Cómo funciona Git

Git es un sistema de control de versiones. **VCS (Version Control System)**

### Sistema de control de versiones

Es un sistema que nos permite registrar los cambios realizados sobre un archivo a lo largo del tiempo, es decir, es como un historial de cambios.

Ya que con git podrás moverte a cualquier versión como si fuera una máquina del tiempo.

![Qué es Git](./images/image-01.png)

Se puede ver como Git guarda solo los nuevos cambios realizados sobre el archivo y no todo el archivo.

### Instalación de Git
    
  * Para Windows:
    
    Entrar a esta [link](https://git-scm.com/downloads) para descargar la última versión de Git disponible.

    Para instalar git es el típico siguiente y siguiente hasta que este instalada.

  * Para Mac:

    Primero debes instalar homebrew (entra a este [link](https://brew.sh/))
    
    Homebrew es un gesto de paquetes para mac. Te recomiendo que lo instales y aprendas a usarlo.

    Abre la terminal y copia el siguiente comando (este comando también se encuentra en la página de homebrew).

    ```bash
      /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
    ```

    Luego de haber instalado homebrew, pasaremos a instalar git

    ```bash
      brew install git
    ```

  Una vez terminemos de instalar git, en ambos sistemas operativos abriremos la terminal y comprobaremos que git se haya instalado correctamente y debería mostrar esto, la versión puede cambiar.
    
  ```bash
    git --version
    git version 2.24.0
  ```

### Configuración de Git

Configuración del usuario

```bash
  git config --global user.email user@example.com
  git config --global user.name "Mauro Quinteros"
```

Ver la lista de configuraciones

```bash
  git config --list
```

### Beneficios de Git

  * Velocidad Puedes trabajar fluidamente desde tu computador.
  * Diseño sencillo El codigo es robusto con las herramientas necesarias, como viajar en el tiempo.
  * Fuerte apoyo en el desarrollo no lineal No trabaja de manera lineal, la linea del tiempo tiene bifurcaciones de manera independiente al proyecto principal.
  * Completamente distribuido Cada quien puede tener una copia del proyecto.
  * Capaz de manejar grandes proyectos Linux, Django, Laravel, etc. Usan git.

<div align="right">
  <a href="#introducción-a-git-y-github">volver al inicio</a>
</div>

## 2. Áreas de trabajo de Git

* **Working Directory**

  Es un área donde se extraen los archivos de la base de datos de git y se colocan en el disco duro para que se usen o modifiquen. También están los archivos que no tienen seguimiento por git.

* **Staging Area**

  Es un área intermedia entre el Working Directory y el Git Directory. Una vez agregues un archivo a esta área, git empezará hacerle seguimiento en caso ocurra otro cambio. Los cambios guardados en esta área son temporales para hacerlos de manera definitiva debes guardarlos en el Git Directory.

* **Git Directory**

  Es donde Git almacena los metadatos y la base de datos para su proyecto. Esta es la parte más importante de Git. Es la parte más importante de Git, y es lo que se copia cuando clonas un repositorio desde otro ordenador.

![Áreas de trabajo de git](./images/image-02.png)

<div align="right">
  <a href="#introducción-a-git-y-github">volver al inicio</a>
</div>

## 3. Los estados de un archivo

* **Estado Untracked**

  Son los archivos que estan sin rastrear y aún no han sido afectados por `git add`, por lo que no git no tiene registros de su existencia.

* **Estado Tracked**

  Son los archivos que viven dentro de git, no tienen cambios pendientes y sus últimas actualizaciones han sido guardadas en el repositorio.

* **Estado Staged**

  Son archivos en staging. Viven dentro de git y hay registro de ellos porque han sido afectados por el comando `git add`.

* **Estado Unstaged**

  Se entienden como archivos ***tracked pero unstaged***. Archivos que viven dentro de git pero no han sido afectados por el comando `git add` ni mucho menos por `git commit`. Git tiene un registro de estos archivos pero esta desactualizado, sus últimas versiones solo están en el disco duro.

![Los 3 estados de un archivo](./images/image-03.png)

<div align="right">
  <a href="#introducción-a-git-y-github">volver al inicio</a>
</div>

## 4. Flujo básico de trabajo de Git

* Iniciamos con el comando `git init` que nos crea un repositorio (crea el archivo **.git** donde se guardará todo el historial de cambios).

* Luego de haber realizado algunos cambios dentro de los archivos 

<div align="right">
  <a href="#introducción-a-git-y-github">volver al inicio</a>
</div>

