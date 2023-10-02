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

## Historial de commits

## Deshacer git add

## git rm

## git mv

## Crear una rama y cambiar a ella

## Fusionar ramas 

## Cómo hacer un push



