# Sistema de control de versiones _git_

## 1. DEFINICIONES 📖

---

-   **`repositorio`** = Es el sistema de control de versiones de tu proyecto
-   **`commit`** : Captura instantanea de los cambios preparados en ese momento
-   **`branch`** : Rama del repositorio
-   **`tracked`**: Que tiene seguimiento de sus cambios
-   **`untracked`**: Que no tiene seguimiento de sus cambios
-   **`status`** : Estado actual del repositorio
-   **`staged`**: Son los archivos que actualmente viven en el staging area
-   **`staging area`** : Lugar donde temporalemente se guardan los cambios del proyecto antes de ser llevados al repositorio

## 2. FLAGS 🚩

---

Nos permite enviar mas informacion en los comandos

-v = version abreviada de las flag
--version = version completa de la flag

## 3. COMANDOS BÁSICOS📓

---

-   **`git init`** = crea un repositorio vacio

-   **`git --version`** = devuelve la version actual de git instalada.

-   **`git clone`** = clona un repositorio en el directorio indicado.

-   **`git help`** = muestra las opciones disponibles para el comando git.

-   **`git config`** = modifica la configuracion del usuario.

-   **`git branch -m <antiguo> <nuevo> `**= renombra la rama actual.

-   **`git status`** = Devuelve informacion de la rama actual.

-   **`git add <fileName>`** = Le da seguimiento a los archivos o carpetas del proyecto.

-   **`git rm --cached`** = mueve los archivos que seleccionamos al estado untracked

-   **`git rm --force`** = elimina los archivos de git y disco duro, git guarda el registro de la existencia de los archivos.

-   **`git reset <fileName>`** = Deshace los cambios locales en el estado (staged to unStaged) de un repositorio de git

-   **`git log`** = Muestra todos lo commits realizados en el repositorio en la rama actual

-   **`git checkout -- .`** = reconstruye el proyecto a como estaba en el ultimo commit

-   **`git checkout -b <BranchName>`** = Crea una nueva rama y te pone en ella

-   **`git fetch <BranchName>`** = Obtener los cambios realizados en la rama clonada.

-   **`git pull`** = actualiza los cambios realizados en la rama clonada.

-   **`git add \*.extension`** = agrega al stage todos los archivos de la misma extension.

-   **`git diff`** = Compara las diferancias en los archivos actuales que no estan en el stage con el ultimo commit.

## 4. CONFIGURACIONES DEL USUARIO 🤵‍♂️

---

-   **`git config --global user.name "<userName>"`** = establece el nombre asociado a git de forma global.

-   **`git config --global user.email <userEmail>`**

-   **`git config --global init.defaultBranch <BranchName>`** = establece el rama inicial por defecto al crear un repositorio

-   **`git config core.autocrlf true`** = Colocar en true cuando haya problemas en con las lineas de termino de archivos (line endings)

## 5. ARCHIVOS ESPECIALES DE GIT 📁

---

-   **`.gitignore`** = Lugar donde se indica que archivos deben ser ignorados por git

-   **`.gitkeep`** = se crea usualmente en carpetas sin contenido para avisarle a git que las mantenga, por defecto git ignora carpetas sin contenido

## 6. PREGUNTAS FRECUENTES 💡

---

**❓ Como inicializar el repositorio de git?.**

➡️ Con el comando `git init` se crea un nuevo repositorio de git.

**❓Como actualizar el mensaje de un commit ya hecho?.**

➡️ Si se necesita modificar el mensaje del ultimo commit realizado, basta con utilizar `git commit --amend -m "<Nuevo mensaje actualizado>"` la bandera -m permite escribir en el mismo comando.
