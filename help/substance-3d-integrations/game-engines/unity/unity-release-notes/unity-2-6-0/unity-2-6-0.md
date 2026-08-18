---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-6-0.html"
breadcrumb-title: ''
description: Revise las notas de la versión 2.6.0 del plugin Unity para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.6.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.6.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---


# Unity 2.6.0

Publicado el 7 de junio de 2021

Actualizado/agregado:

* Nuevo flujo de trabajo para acceder al Substance Source La acción del Substance Source ahora accede a la pestaña Origen dentro del Iniciador de Substance, lo que permite enviar los recursos directamente a Unity
* La información de la versión del plugin se puede copiar en el portapapeles
* Eliminación de &quot;Generar al cargar&quot; de la configuración de destino

Correcciones:

* En los proyectos HDRP, el modo de Desplazamiento volverá al valor predeterminado (Tessallation) cuando se realice un cambio en el ajuste del material
* El tamaño de la resolución no se muestra en la ventana del inspector
* No se puede instalar el complemento en las versiones de Unity 2020.2 y posteriores

Problemas conocidos:

* Se produce un error de acceso denegado o un bloqueo al actualizar el plugin de versiones anteriores (2.5.4 y anteriores)
  * Solución alternativa: Las versiones de plugins anteriores 2.5.4 y anteriores, deben desinstalarse desde las versiones de proyecto de Unity 2020.2 y posteriores antes de instalar el plugin 2.6.0
* Las vistas previas de textura de archivos de imagen no se mostrarán en el inspector cuando esté instalado el plugin de Substance
  * El origen de este problema existe en Unity y está previsto que Unity lo corrija en sus versiones 2021.2 (actualmente en versión beta)
