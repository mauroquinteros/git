# Introducción a Git y GitHub

## Contenido
Este repositorio es un resumen del [curso de Git y Github](https://platzi.com/cursos/git-github/) en Platzi 💚

Si deseas aportar a este repositorio puedes hacer un pull request una vez hayas terminado de leer este resumen.

 1. Cómo funciona Git
  - [Instalación](###Instalación-de-Git)
  - [Configuración](###Configuración-de-Git)
  - [Beneficios](###Beneficios-de-Git)
 2. Áreas de trabajo de Git
 3. Flujo básico de trabajo de git
 4. Los estados de un archivo
 5. Comandos Básicos de git
 6. Manejo de ramas (branch) en Git
 7. Flujo de trabajo profesional usando Github
 8. Manejo de los pull requests y forks

## 1. Cómo funciona Git

Git es un sistema de control de versiones. **VCS (Version Control System)**

### Sistema de control de versiones

Es un sistema nos permite registrar los cambios realizados sobre un archivo a lo largo del tiempo, es decir, es como un historial de cambios.

Ya que con git podrás moverte a cualquier versión como si fuera una máquina del tiempo.

![Qué es Git](./images/image-01.png)

Se puede ver como Git guarda solo los nuevos cambios realizados sobre el archivo y no sobre todo el archivo.

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

  <div align="right">
    <a href="#contenido">volver al inicio</a>
  </div>

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

## 2. Áreas de trabajo de Git

* **Working Directory**

  Es el área donde Git no tiene idea de los cambios que has realizado, ya que Git no le está haciendo seguimiento. Los archivos que estan en esta área están guardados en tu disco duro.

* **Staging Area**

  Es un área intermedia entre el Working Directory y el Git Directory. Una vez agregues un archivo a esta área, git empezará hacerle seguimiento en caso ocurra otro cambio. Los cambios guardados en esta área son temporales para hacerlos de manera definitiva debes guardarlos en el Git Directory.

* **Git Directory**

  Es donde Git almacena la base de datos de los cambios sobre tu proyecto. Es la parte más importante de Git, y es lo que se copia cuando clonas un repositorio desde otro ordenador.

## 3. Flujo básico de trabajo de Git

* Iniciamos con el comando `git init` que nos crea un repositorio (crea el archivo **.git** donde se guardará todo el historial de cambios).

* Luego de haber realizado algunos cambios dentro de los archivos 
