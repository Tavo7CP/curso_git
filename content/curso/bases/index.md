---
title: "Las bases de Git"
date: 2020-08-08
draft: false
description: "Aprende lo más básico."
slug: ""
tags: [""]
series: ["Curso"]
series_order: 6
---

# Lo básico de lo básico.

## Configurando Git por primera vez en un equipo.

``` bash
git config --list --show origin
```

Este comando muestra una lista con las configuraciones que están en el equipo.

Para modificar las configuraciones se utilizan los comandos:

Para configurar el usuario.
``` bash
git config --global user.name "<usuario>"
```

Para configurar el correo electrónico.
``` bash
git config --global user.email correo@dominio.com 
```


## Pidiendo ayuda.

Para obtener ayuda acerca de qué hace determinado comando de Git, utilizamos 

``` bash
git help <verbo>
```

Por ejemplo, para obtener ayuda del comando "add", se utiliza:

``` bash
git help add
```

