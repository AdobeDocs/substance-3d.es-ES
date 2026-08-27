---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/3ds-max/3ds-max-plugin-release-notes/3ds-max-2-7-0.html"
breadcrumb-title: ''
description: Revise las notas de la versión 2.7.0 del plugin 3ds Max para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Substance 3D Integrations
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3ds Max 2.7.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# 3ds Max 2.7.0

<b>Agregado/actualizado:</b>

* Se ha actualizado el motor del Substance a la versión 9 en el plugin 3ds Max, lo que mejora el rendimiento y la compatibilidad.

<b>Corregido:</b>

* Se ha solucionado un problema de bloqueo en las versiones de 3ds Max 2019, 2022, 2023 y 2024, por el que, al arrastrar un nodo de Substance 2 al Editor de material de Slate, el programa se bloqueaba. El nodo de Substance 2 ahora se puede arrastrar y soltar de forma segura en el editor de materiales de Slate.
* Se ha resuelto un problema en el plugin de Substance para 3ds Max, donde al seleccionar &quot;Substance a Arnold&quot; y otros flujos de trabajo no se creaban nodos relevantes en el Editor de Material Slate, sino que se abría erróneamente un Maxscript con un error de compilación. Los nodos para flujos de trabajo como Arnold ahora se generan y conectan correctamente de forma automática.
* Se solucionó un problema por el que la exportación de recursos/ajustes preestablecidos de inicio (.sbsar - mapa de textura de Substance2) desde Substance 3D Sampler y su conversión al procesador Corona (versiones 6 a 9hf1) dentro de 3ds Max provocaba materiales dañados, procesamiento con color base negro y normales de relieve rotos. Además, esta actualización soluciona la inaccesibilidad de la ficha de propiedades del Substance en los materiales, un problema que también afectaba a las conversiones a Vray.
* Se ha solucionado un problema en el plugin 3ds Max por el que el plugin para conectar o desconectar entradas de texturas de Substance2 en Corona Material provocaba bloqueos.
* Se solucionó el problema de compatibilidad en 3ds Max 2024, donde las secuencias de comandos de Python incrustadas o llamadas dentro de un archivo MaxScript no se permitían de forma predeterminada.
* Se ha solucionado un problema en el plugin 3Ds Max por el que, al importar y ejecutar el plugin Substance a Corona, los materiales aparecían en negro y brillantes en las previsualizaciones y representaciones de sombreado. Este problema se ha solucionado ahora correctamente, lo que garantiza la visualización y el procesamiento correctos de los mapas de Substance con el procesador de Corona.

Esta versión se ha lanzado para 3ds Max 2021, 2022 y 2023
