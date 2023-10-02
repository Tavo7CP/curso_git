---
title: "Comandos para el uso personal de Git"
date: 2020-08-08
draft: false
description: "Aprende lo más básico."
slug: ""
tags: [""]
series: ["Curso"]
series_order: 3
---


## Moviéndose en la terminal.
**cd (Change Directory):**

Descripción: Este comando se utiliza para cambiar el directorio actual en el que te encuentras en la terminal.

Uso básico: cd nombre-de-directorio (cambia al directorio especificado) o cd .. (cambia al directorio padre).

Ejemplo: cd Documentos te llevará al directorio "Documentos" si existe en el directorio actual.

**ls (List):**

Descripción: ls se utiliza para listar los archivos y directorios en el directorio actual.

Uso básico: ls [opciones] [nombre-de-directorio] (si no se proporciona un nombre de directorio, lista el contenido del directorio actual).

Ejemplo: ls -l mostrará una lista detallada de archivos y directorios.

**mkdir (Make Directory):**

Descripción: mkdir se utiliza para crear un nuevo directorio (carpeta).

Uso básico: mkdir nombre-de-directorio (crea un directorio con el nombre especificado en el directorio actual).

Ejemplo: mkdir MiNuevoDirectorio creará un nuevo directorio llamado "MiNuevoDirectorio".

## Inicializar repositorio

Nos situamos en el directorio donde trabajaremos y escribimos el comando

``` bash
git init
```
## Agregar archivos a la zona de rastreo.

Para esto, solo debemos agregar los archivos mediante el comando 

``` bash
git add <archivo>
```

## git status

git status es un comando que se utiliza para mostrar el estado actual de nuestro repositorio. Proporciona información sobre los cambios que hemos realizado en los archivos y cómo se encuentran en relación con el control de versiones. En resumen, git status muestra:

* Los archivos que han sido modificados desde el último commit.
* Los archivos que están en el área de preparación (staging) listos para ser incluidos en el próximo commit.
* Los archivos que no están siendo rastreados por Git.

## .gitignore

Aquí hay un ejemplo de de un archivo .gitignore

``` bash
# Ignorar archivos de respaldo generados por editores de texto
*~

# Ignorar archivos de registro
*.log

# Ignorar archivos y directorios de construcción
/build/
/dist/
/node_modules/ 
```


## Commit
Una vez que todos los archivos que se desean agregar están en la etapa de stage, se utiliza el comando

``` bash
git commit -m "mensaje descriptivo del commit"
```

## Historial de commits

Para revisar el historial de commits utilizamos

``` bash
git log
```

## Deshacer git add
Utilizar

``` bash
git reset mi-archivo.txt
```
eliminará "mi-archivo.txt" de la zona de preparación, pero el archivo seguirá estando en tu directorio de trabajo y no se verá afectado por esta operación.
## git rm
El comando git rm se utiliza para eliminar archivos de seguimiento en Git y también para marcarlos como "eliminados" en la zona de preparación (stage). Puedes usarlo para eliminar archivos tanto del sistema de archivos como del control de versiones de Git al mismo tiempo.

La sintaxis básica es:

``` bash
git rm nombre-de-archivo
```

## git mv

El comando git mv se utiliza para renombrar o mover archivos en un repositorio Git. Al utilizar este comando, Git registra el cambio de nombre o movimiento de un archivo, lo que ayuda a mantener el historial de versiones de manera precisa. La sintaxis básica es:

``` bash
git mv archivo-antiguo archivo-nuevo
```
## Crear una rama y cambiar a ella
Para realizar esto solo necesitamos utilizar el comando:

``` bash
git checkout -b nombre_de_la_rama
```

## Fusionar ramas 

El comando **git merge** se utiliza para combinar los cambios de una rama en otra. Esto significa que podemos tomar los cambios realizados en una rama y fusionarlos en otra rama, lo que es especialmente útil cuando trabajamos en proyectos colaborativos o cuando deseamos incorporar nuevas características desarrolladas en una rama de desarrollo en la rama principal del proyecto.

La sintaxis básica del comando git merge es la siguiente:

``` bash
git merge nombre-de-la-rama

```

## Crear llaves para GitHub

### ¿Tenemos llaves?

``` bash
$ ssh-add -l -E sha256
> 2048 SHA256:274ffWxgaxq/tSINAykStUL7XWyRNcRTlcST1Ei7gBQ /Users/USERNAME/.ssh/id_rsa (RSA)
```

El comando ssh-add debe imprimir una cadena larga de números y letras. Si no imprime nada, debemos generar una nueva clave SSH y asociarla a GitHub.

### Generación de llaves

Desde terminal escribimos
``` bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```
y solo presionamos enter a todo.
Ahora toca agregar la clave SSH al ssh-agent

1. Primero se inicia el agente SSH en segundo plano
``` bash
$ eval "$(ssh-agent -s)"
> Agent pid 59566

```
2. Se agrega la llave privada SSH al ssh-agent.
``` bash
ssh-add ~/.ssh/id_ed25519
```

3. Se utiliza el siguiente comando para obtener la llabe SSH
``` bash
$ cat ~/.ssh/id_ed25519.pub
```
Se copia la llave que se muestra.

En el perfil de GitHub > Settings > sección "Acceso" de la barra lateral > clic en Claves SSH y GPG.

En el campo "Title" (Título), agregamos una etiqueta descriptiva para la clave nueva. Por ejemplo, si estamos utilizando un portátil personal, podemos llamar a esta clave "Portátil personal". El tipo de clave lo dejamos como autenticación. En el campo "Clave", pegamos la clave pública. Y clic en Agregar clave SSH.

## Sincronización de repositorios

Una vez que tenemos nuestro repositorio listo para subir a GitHub, necesitamos:

1. Acceder a la plataforma.
2. Crear un repositorio con el mismo nombre.
3. Utilizar los siguientes comandos en la terminal:
   
``` bash
git remote add origin https://github.com/Usuario/nomre_repo.git
git branch -M main
git push -u origin main
```
Este primer push se utiliza para subir todo lo que tenemos al repositorio.

## Cómo hacer un push
Una vez que nuestros respositorios están sincronizados, solo necesitamos ejecutar

``` bash
git push
```
para subir los cambios realizados.


