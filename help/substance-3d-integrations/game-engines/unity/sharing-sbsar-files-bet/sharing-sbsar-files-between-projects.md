---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/game-engines/unity/sharing-sbsar-files-between-projects.html"
breadcrumb-title: ''
description: Comparta archivos SBSAR de Substance entre proyectos de Unity y conserve los ajustes de parámetros mediante archivos de ajustes preestablecidos.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity >Sharing sbsar Files Between Projects
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Compartir archivos sbsar entre proyectos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# Compartir archivos sbsar entre proyectos

Es posible compartir archivos .sbsar entre proyectos y equipos manteniendo los mismos ajustes de parámetros con el uso de archivos .sbsprs.

Una vez que el material del proyecto original se haya modificado a los ajustes que se compartirán, vaya a los ajustes preestablecidos en el panel del inspector. En los ajustes preestablecidos, cree un nuevo ajuste preestablecido y asígnele un nombre. Este nuevo ajuste preestablecido con nombre aparecerá en la lista de ajustes preestablecidos para este material. Una vez hecho esto, exporte el ajuste preestablecido para guardarlo localmente.

Cuando utilice el archivo .sbsar en otro proyecto o equipo, incluya también el archivo de ajustes preestablecidos exportado. Una vez importada la barra base en el proyecto Unity, vaya a los ajustes preestablecidos y elija la opción de importación. Seleccione el archivo de ajustes preestablecidos del paso anterior e impórtelo. Se debe añadir a la lista de ajustes preestablecidos un ajuste preestablecido con los ajustes del proyecto anterior.

Repita el proceso para todos los materiales que se compartan.
