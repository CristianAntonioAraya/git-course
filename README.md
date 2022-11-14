# Sistema de control de versiones _git_

## [ÍNDICE](#indice)

1. [Definiciones](#id1)
2. [Flags o Banderas](#id2)
3. [Comandos Básicos](#id3)
4. [Configuraciones del usuario](#id4)
5. [Recomendaciones para un buen commit](#id5)
6. [Archivos especiales de Git](#id5)
7. [Preguntas frecuentes](#id7)
    - [Como inicializar el repositorio de git?.](#q1)
    - [Como agregar archivos al stage area?.](#q2)
    - [Como actualizar el mensaje de un commit ya hecho?.](#q3)
    - [Como puedo ver el historial de commits?.](#q4)
    - [Como podemos volver en el tiempo a un commit anterior?.](#q5)
    - [Cúal es el ID o Hash de un commit?.](#q6)

<div id='id1' />

---

## 1. DEFINICIONES 📖

-   **`repositorio`** : Es el sistema de control de versiones de tu proyecto
-   **`commit`** : Captura instantanea de los cambios preparados en ese momento
-   **`branch`** : Rama del repositorio
-   **`tracked`**: Que tiene seguimiento de sus cambios
-   **`untracked`**: Que no tiene seguimiento de sus cambios
-   **`status`** : Estado actual del repositorio
-   **`staged`**: Son los archivos que actualmente viven en el staging area
-   **`working directory`**: Es el area donde se desarrolla el proyecto.
-   **`staging area`** : Lugar donde temporalemente se guardan los cambios del proyecto antes de ser llevados al repositorio o regresados

<div id='id2' />

---

## 2. FLAGS 🚩

Las flags o banderas nos permiten agregarles caracteristicas a los comandos, dichas banderas suelen tener una version corta.

✅Ejemplo:

Para el comando `git log` que devuelve el historial de commit

En el comando `git log --patch`, --patch seria la bandera de este comando,para `git -p` que es el mismo comando -p seria la version abreviada de --patch.

<div id='id3' />

---

## 3. COMANDOS BÁSICOS📓

-   **`git init`** : crea un repositorio vacio

-   **`git --version`** : devuelve la version actual de git instalada.

-   **`git clone`** : clona un repositorio en el directorio indicado.

-   **`git help`** : muestra las opciones disponibles para el comando git.

-   **`git config`** : modifica la configuracion del usuario.

-   **`git branch -m <antiguo> <nuevo> `**: renombra la rama actual.

-   **`git status`** : Devuelve informacion de la rama actual.

-   **`git add <fileName>`** : Le da seguimiento a los archivos o carpetas del proyecto.

-   **`git rm`** : Este comando nos ayuda a eliminar archivos de git sin eliminar su historial del sistema de versiones, este commando necesita funcionar con una de las dos banderas disponibles.

-   **`git rm --cached`** : Elimina los archivos de nuesto repositorio local y staging area, pero lo mantiene en nuestro disco duro.

-   **`git rm --force`** : Elimina los archivos de git y disco duro, se requeriran comandos mas avanzados para poder recuperarlos

-   **`git reset <fileName>`** : Deshace los cambios locales en el estado (staged to unStaged) de un repositorio de git

-   **`git log`** : Muestra todos lo commits realizados en el repositorio en la rama actual

-   **`git checkout -- .`** : reconstruye el proyecto a como estaba en el ultimo commit

-   **`git checkout -b <BranchName>`** : Crea una nueva rama y te pone en ella

-   **`git fetch <BranchName>`** : Obtener los cambios realizados en la rama clonada.

-   **`git pull`** : actualiza los cambios realizados en la rama clonada.

-   **`git add \*.extension`** : agrega al stage todos los archivos de la misma extension.

-   **`git diff`** : Compara las diferancias en los archivos actuales que no estan en el stage con el ultimo commit.

---

<div id='id4' />

## 4. CONFIGURACIONES DEL USUARIO 🤵‍♂️

-   **`git config --global user.name "<userName>"`** : establece el nombre asociado a git de forma global.

-   **`git config --global user.email <userEmail>`** : Establece el email asociado a git de forma global.

-   **`git config --global init.defaultBranch <BranchName>`** : establece el rama inicial por defecto al crear un repositorio

-   **`git config core.autocrlf true`** : Colocar en true cuando haya problemas en con las lineas de termino de archivos (line endings)

---

<div id='id5' />

## 5. Recomendaciones para un buen commit 📝

### Estructura Básica🚧

➡️ Usualmente el mensaje de commit se divide en 3 partes, _titulo_, _cuerpo_ y _pie_

```
    [Titulo] => [tipo]: asunto

    [Cuerpo]

    [Pie]
```

### Tipos/Type 📘

-   **[add]**: Se agregaron archivos.
-   **[delete]**: Se eliminaron archivos.
-   **[test]**: Cambios en los archivos de testeo \*/test.
-   **[dist]**: Cambios en los modulos del proyecto.
-   **[minor]**: Pequeños cambios en el proyecto.
-   **[doc]**: Cambios en la documentación.
-   **[fix]**: Correción de errores.
-   **[bin]**: Cambios en los scripts binarios asociados con el proyecto.
-   **[refactor]**: Refactorización de codigo existente.
-   **[nit]**: Pequeños cambios relacionados a estilo o sintaxis
-   **[feat]**: Nuevas caracteristicas

### Asunto/Subject 📧

➡️ Usualmente contiene aproximadamente 50 caracteres, se inicia con mayuscula y no termina con punto, Se escribe en modo imperativo, y la mejor práctica esque debe ser en inglés.

### Body/Cuerpo 📝

➡️ Se utiliza para explicar el ¿Qué? y ¿Por qué? del commit y no el ¿Cómo?, Al escribir el cuerpo, requerimos de una línea en blanco entre el título y el cuerpo

## Footer/Pie 👣

➡️ Esta parte es muy importante ya que es donde se coloca el seguimiento de los issues o tickets relacionados con los cambios generados.

## Ejemplo

```
📚 DOCS: Changes in README file

Se agrego mas informacion en la documentacion del proyecto,

Issue: 1#
```

## <div id='id6' />

---

## 6. ARCHIVOS ESPECIALES DE GIT 📁

-   **`.gitignore`** : Lugar donde se indica que archivos deben ser ignorados por git

-   **`.gitkeep`** : se crea usualmente en carpetas sin contenido para avisarle a git que las mantenga, por defecto git ignora carpetas sin contenido

<div id='id7' />

---

## 7. PREGUNTAS FRECUENTES 💡

---

## <div id='q1' />

**_❓ Como inicializar el repositorio de git?._**

➡️ Con el comando:

```
git init
```

Con esto se crea el repositorio del proyecto con la configuracion inicial, creando a su vez un sub directorio con extension .git en tu directorio de trabajo actual, este archivo aparece *oculto* en la raiz de tu proyecto.

<br>

**[⬆ Volver a índice](#índice)**

---

## <div id='q2'>

**_❓Como agregar archivos al stage area?._**

➡️ El área de staging se puede ver como un limbo donde nuestro archivos están por ser enviados al repositorio o ser regresados a la carpeta del proyecto.

Para ver si un archivo o carpeta pertenece o no al staging area, hace falta ejecutar el comando

```
git status
```

<br>

**[⬆ Volver a índice](#índice)**

---

## <div id='q3'>

**_❓Como actualizar el mensaje de un commit ya hecho?._**

➡️ Si se necesita modificar el mensaje del ultimo commit realizado, basta con utilizar

```
git commit --amend -m "<Nuevo mensaje actualizado>"
```

la bandera -m permite escribir en el mismo comando.

---

## <div id='q4'>

**❓ Como puedo ver el historial de commits?.**

➡️ Para mostrar los commits realizados en todas las ramas, se utiliza el comando:

```
git log
```

Este comando tiene la posibilidad de agregarles decenas de banderas, entre ellas y a las mas usadas son:

-   `--oneline`: Permite ver el historial de commits pero resumidos cada uno en una linea.
-   `--all`: Permite ver el historial de commits de todas las ramas, incluso las que aun no se han unido a la principal.
-   `--author="username or email"` Permite filtrar el historial de commits por usuario o email.
-   `-<n>`: n es la cantidad de commits que se mostraran desde el mas reciente hacia atras.

<br>

**[⬆ Volver a índice](#índice)**

---

## <div id='q5'>

**❓ Como podemos volver en el tiempo a un commit anterior?.**

➡️ Hay 2 maneras de volver a un estado anterior del repositorio, una de ellas.

```
git checkout + ID del commit
```

Nos permite volver a cualquier versión anterior de un archivo específico o incluso del proyecto entero.

El otro método un tanto mas "rudo" es con el comando

```
git reset
```

La principal diferencia con checkout esque no solo "volveremos en el tiempo", sino que borraremos los cambios que hicimos despues de este commit.

Existen tres formas de usar este comando, con la bandera `--hard` que borra toda la informacion que tengamos en el staging area, y la que es un poco mas segura `--soft` que mantiene dicha informacion para que los cambios realizados sean aplicados desde un punto anterior y por ultimo `--mixed` que elimina los cambios hasta el working area.

Utilizar `git checkout` lo mas posible, pero si es estrictamente necesario usar `git reset` procure dominarlo para no caer en errores irreversibles.

<br>

**[⬆ Volver a índice](#índice)**

---

## <div id='q6'>

**❓ Cúal es el ID o Hash de un commit?.**

➡️ Para identificar un commit, existe el ID de este, este ID se forma gracias a una funcion criptografica conocida como SHA-1 que codifica informacion del commit.

📨 Esto incluye:

-   Todo el contenido del commit.
-   El ID del commit previo.
-   La fecha del commit.
-   Nombre y correo del autor.
-   Mensajes de registro.

✳️ Ejemplo de un commit realizado en este repositorio.

```
Commit completo ⬇️ (git log)

    commit 9d2cdf3a12400cfaf9aa0c8fb0aa4e688f04a9cf (HEAD -> Production, origin/Production, origin/HEAD)
    Author: CristianAntonioAraya <dev.arayacristian@gmail.com>
    Date:   Sun Nov 13 15:25:36 2022 -0300

        Docs: Add example on commits recomendation

Commit Abreviado ⬇️(git log --oneline)

    9d2cdf3 Docs: Add example on commits recomendation
```

Tanto **`9d2cdf3a12400cfaf9aa0c8fb0aa4e688f04a9cf`** en el commit completo como **`9d2cdf3`** en el commit abreviado, son el identificador del mismo commit, cualquiera de los dos sirven para ser usados en comandos.

<br>

**[⬆ Volver a índice](#índice)**

---
