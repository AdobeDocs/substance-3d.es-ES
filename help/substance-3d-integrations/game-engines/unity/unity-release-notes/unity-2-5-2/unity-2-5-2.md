---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-5-2.html"
breadcrumb-title: ''
description: Revise las notas de la versión 2.5.2 del plugin Unity para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.5.2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.5.2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# Unity 2.5.2

Publicado el 23 de julio de 2020

Añadido:

* Función &quot;IsProcessing()&quot; que indica si el procesador está ocupado o inactivo (no ocupado)

Corregido:

* Ya no se muestra un error al establecer la configuración de abrazadera 2048 y destino 4096
* Las propiedades de los materiales se transferirán al actualizar a HDRP y/o URP desde Standard
* Los scripts que modifican los materiales del Substance funcionarán según lo previsto al implementarse en dispositivos móviles
* El canal rojo ya no se copia en el Alpha y el Alpha predeterminado se establece en blanco
* Bloqueo al modificar la configuración de destino en Mac
* Se ha eliminado el error NullReferenceException al crear material de Unity
* Se ha eliminado el error al salir del modo de reproducción después de editar las propiedades de mosaico
* Habilitar la creación de instancias de GPU se puede activar
* Los materiales que utilizan Transparencia no desaparecerán o se volverán negros de forma incorrecta cuando exista el Modo de reproducción
* Los materiales de Substance no se destruirán en el proyecto HDRP al actualizar el plugin
