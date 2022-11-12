# Sistema de control de versiones _git_

## ÍNDICE

1. [Definiciones](#id1)
2. [Flags o Banderas](#id2)
3. [Comandos Básicos](#id3)
4. [Configuraciones del usuario](#id4)
5. [Archivos especiales de git](#i5)
6. [Preguntas frecuentes](#id6)

<div id='id1' />

## 1. DEFINICIONES 📖

---

-   **`repositorio`** : Es el sistema de control de versiones de tu proyecto
-   **`commit`** : Captura instantanea de los cambios preparados en ese momento
-   **`branch`** : Rama del repositorio
-   **`tracked`**: Que tiene seguimiento de sus cambios
-   **`untracked`**: Que no tiene seguimiento de sus cambios
-   **`status`** : Estado actual del repositorio
-   **`staged`**: Son los archivos que actualmente viven en el staging area
-   **`staging area`** : Lugar donde temporalemente se guardan los cambios del proyecto antes de ser llevados al repositorio

<div id='id2' />

## 2. FLAGS 🚩

---

Las flags o banderas nos permiten agregarles caracteristicas a los comandos, dichas banderas suelen tener una version corta.

✅Ejemplo:

Para el comando `git log` que devuelve el historial de commit

En el comando `git log --patch`, --patch seria la bandera de este comando,para `git -p` que es el mismo comando -p seria la version abreviada de --patch.

<div id='id3' />

## 3. COMANDOS BÁSICOS📓

---

-   **`git init`** : crea un repositorio vacio

-   **`git --version`** : devuelve la version actual de git instalada.

-   **`git clone`** : clona un repositorio en el directorio indicado.

-   **`git help`** : muestra las opciones disponibles para el comando git.

-   **`git config`** : modifica la configuracion del usuario.

-   **`git branch -m <antiguo> <nuevo> `**: renombra la rama actual.

-   **`git status`** : Devuelve informacion de la rama actual.

-   **`git add <fileName>`** : Le da seguimiento a los archivos o carpetas del proyecto.

-   **`git rm --cached`** : mueve los archivos que seleccionamos al estado untracked

-   **`git rm --force`** : elimina los archivos de git y disco duro, git guarda el registro de la existencia de los archivos.

-   **`git reset <fileName>`** : Deshace los cambios locales en el estado (staged to unStaged) de un repositorio de git

-   **`git log`** : Muestra todos lo commits realizados en el repositorio en la rama actual

-   **`git checkout -- .`** : reconstruye el proyecto a como estaba en el ultimo commit

-   **`git checkout -b <BranchName>`** : Crea una nueva rama y te pone en ella

-   **`git fetch <BranchName>`** : Obtener los cambios realizados en la rama clonada.

-   **`git pull`** : actualiza los cambios realizados en la rama clonada.

-   **`git add \*.extension`** : agrega al stage todos los archivos de la misma extension.

-   **`git diff`** : Compara las diferancias en los archivos actuales que no estan en el stage con el ultimo commit.

<div id='id4' />

## 4. CONFIGURACIONES DEL USUARIO 🤵‍♂️

---

-   **`git config --global user.name "<userName>"`** : establece el nombre asociado a git de forma global.

-   **`git config --global user.email <userEmail>`** : Establece el email asociado a git de forma global.

-   **`git config --global init.defaultBranch <BranchName>`** : establece el rama inicial por defecto al crear un repositorio

-   **`git config core.autocrlf true`** : Colocar en true cuando haya problemas en con las lineas de termino de archivos (line endings)

<div id='id5' />

## 5. ARCHIVOS ESPECIALES DE GIT 📁

---

-   **`.gitignore`** : Lugar donde se indica que archivos deben ser ignorados por git

-   **`.gitkeep`** : se crea usualmente en carpetas sin contenido para avisarle a git que las mantenga, por defecto git ignora carpetas sin contenido

<div id='id6' />

## 6. PREGUNTAS FRECUENTES 💡

---

**_❓ Como inicializar el repositorio de git?._**

➡️ Con el comando `git init` se crea un nuevo repositorio de git.

**_❓Como actualizar el mensaje de un commit ya hecho?._**

➡️ Si se necesita modificar el mensaje del ultimo commit realizado, basta con utilizar `git commit --amend -m "<Nuevo mensaje actualizado>"` la bandera -m permite escribir en el mismo comando.

**❓ Como puedo ver el historial de commits?.**

➡️ `git log` Muestra los commits realizados en el repositorio en todas las ramas, tiene la posibilida de agregarles decenas de banderas, entre ellas y a las mas usadas son:

-   `git log --oneline`: Permite ver el historial de commits pero resumidos cada uno en una linea.
-   `git log --all`: Permite ver el historial de commits de todas las ramas, incluso las que aun no se han unido a la principal.
-   `git log --author="username or email"` Permite filtrar el historial de commits por usuario o email.
-   `git log -<n>`: n es la cantidad de commits que se mostraran desde el mas reciente hacia atras.
