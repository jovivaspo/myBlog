---
title: 'Guía básica de Git'
excerpt: 'Git es un sistema de control de versiones que te permite manejar y rastrear los cambios en tus proyectos de software. Ya sea que estés trabajando solo o en equipo, Git te ayuda a mantener un registro de las modificaciones que has hecho en tus archivos, lo que facilita la colaboración y la resolución de conflictos.

A continuación, te ofrecemos una guía básica de Git para que puedas empezar a trabajar con él de forma eficiente y eficaz. Aprenderás cómo configurar Git, crear un repositorio, realizar cambios, guardar y actualizar tus cambios, y trabajar con repositorios remotos. ¡Vamos a empezar!'
coverImage: '/assets/blog/git-basic/git-basic.webp'
date: '2023-03-17T05:35:07.322Z'
author:
  name: Jorge Vivas
  picture: '/assets/blog/authors/tim.jpeg'
ogImage:
  url: '/assets/blog/git-basic/git-basic.webp'
---
# **Git**

## **¿Qué es Git**

Git es un sistema de control de versiones de código. Es una herramienta que permite a los desarrolladores mantener un registro de los cambios realizados en su código y colaborar de manera efectiva en proyectos de software.

Por ejemplo, con Git, puedes crear un repositorio que contenga todo el historial de cambios en tu proyecto. Cada vez que realizas un cambio en el código, puedes "comitear" ese cambio al repositorio, lo que permite llevar un registro de ese cambio y revertir fácilmente a versiones previas si es necesario.

Además, Git permite trabajar de manera colaborativa en proyectos de software. Puedes clonar repositorios de otros desarrolladores, hacer tus propios cambios y enviarlos de vuelta al repositorio original como "pull request". Esto permite un flujo de trabajo colaborativo y eficiente para el desarrollo de software.

> "Git is a free and open source distributed version
> control system designed to handle everything
> from small to very large projects with speed and
> efficiency”. [Source](https://git-scm.com)

Entre sus características podremos destacar:

- Control de cambios
- Fácil de usar
- Más útil con archivos de texto
- Gestión de funciones
- Trabajo en equipo
- No hay un servidor real
- Equipos remotos
- Implementación en diferentes entornos
- ¡Moderno y en constante evolución!

## **Instalación**

- Enlaces:
  - [Window](https://git-scm.com/download/win)
  - [Mac](https://git-scm.com/download/mac)
  - [Linux](https://git-scm.com/download/linux)
- Configuración:
  - Define Visaul Studio Code como editor por defecto.
  - Define la rama principal como "main".

## **Comandos básicos**

### Configurar git

- **`git config --global user.name "[name]`**: establecer el nombre que quieres adjuntar en tus commit.
- **`git config --global user.email "[email address]"`**: establecer el email que quieres adjuntar en tus commit.

### Iniciar:

- **`git init [project-name]`**: iniciar un repositorio.
- **`git clone [url]`**: clonar un repositorio.

### Stage & Snapshot:

- **`git init`**: iniciar un repositorio.
- **`git status`**: verificar el repositorio, muestra archivos modificados en el directorio de trabajo y listos para hacer commit.
- **`git add [file]`** or **`git add .`** : agregar un archivo o todos los cambios.
- **`git diff`**: diferencias de lo que ha cambiado pero no está en stage.
- **`git commit -m [menssage]`**: hacer commit de los cambios y agregar un mensaje descriptivo.

### Branch & Merge:

- **`git branch`**: listar las ramas, una \* aparece junto a la rama activa actual..
- **`git branch [branch-name]`**: crear una nueva rama.
- **`git checkout [branch-name]`**: seleccionar una rama.
- **`git checkout -b [branch-2] [branch-1]`**: crear una rama llamada branch-2 a partir de la rama branch-1.
- **`git merge [branch]`**: fusionar la rama especificada en la rama actual.
- **`git log`**: mostrar todos los commits en la rama actual.
- **`git log --oneline`**: mostrar todos los commits en una sola línea.

### Share & update:

- **`git remote add [url]`**: añadir url git.
- **`git push [branch]`**: enviar los commits de la rama local a la rama en el repositorio remoto.
- **`git pull [branch]`**: obtener el último commit de la rama remota.

### Tracking path changes:

- **`git rm [file]`**: borrar el archivo del proyecto.
- **`git mv [existing-path] [new-path]`**: cambiar la ruta del archivo existente y preparar el movimiento

### Rewrite history:

- **`git rebase [branch]`**: aplicar cualquier confirmación del branch actual antes de la especificada.
- **`git reset --hard [commit]`**: limpiar el área de preparación y reescribir el árbol de trabajo a partir del commit especificado.

**Más recursos**:

- [Original documentation](https://git-scm.com/docs)
- [Pro Git book](https://git-scm.com/book/en/v2)
- [Git Cheat Sheets](https://training.github.com/) in different lenguages.

## **Graphical Interfaces**

- [SourceTree](https://www.sourcetreeapp.com)
- [GitKraken](https://www.gitkraken.com)

## **Cómo hacer buenos commits**

Hay 7 reglas básicas:

1. Separar el tema del cuerpo con una línea en blanco.
2. Limitar la línea del tema a 50 caracteres.
3. Capitalizar la línea del tema.
4. No terminar la línea del tema con un punto.
5. Usar el modo imperativo en la línea del tema.
6. Envolver el cuerpo en 72 caracteres.
7. Utilizar el cuerpo para explicar qué y por qué en lugar de cómo.

![Cómo hacer un commit correctamente](https://res.cloudinary.com/dme5pqzrj/image/upload/f_auto/v1678192260/git_commit_2x_aoj7oa.png)

[Source](https://chris.beams.io/posts/git-commit/)

## **Git-flow Workflow**:
Git flow es una estrategia popular de ramificación de Git que tiene como objetivo simplificar la gestión de versiones y fue introducida por el desarrollador de software Vincent Driessen en 2010. Fundamentalmente, Git flow implica aislar tu trabajo en diferentes tipos de ramas de Git.

En el flujo de trabajo de Git flow, hay cinco tipos diferentes de ramas:

- Main: contiene código listo para producción que puede ser lanzado.
- Develop: contiene código preproducción con nuevas características desarrolladas que están en proceso de ser probadas.
- Feature: se utiliza al agregar nuevas características a tu código.
- Release: se utiliza al preparar nuevas versiones de producción.
- Hotfix: se utiliza para abordar rápidamente cambios necesarios en tu rama principal.
  ![Git flow](https://www.gitkraken.com/wp-content/uploads/2021/03/git-flow-4.svg)
  [Source](https://www.gitkraken.com/learn/git/git-flow)

### **Pasos para Git-flow básico**:

1.  **Main** branch será la rama para el cliente no para desarrollo.
2.  Crear una branch de  **desarrollo**.
3.  Crear una branch por cada nueva característica, branch [feature-name].
4.  Una vez finalizada la características hacer merge con la branch de **desarrollo**.
5.  Cuando todas las características estén listas, haremos merge con la rama **main** añadiendo una nueva **tag/release**.

## **Conclusión**

En resumen, podríamos decir que Git es una herramienta esencial para cualquier desarrollador de software que desee llevar un control de versiones y colaborar de manera efectiva en proyectos de software.
