---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/guides/performances-and-optimizations.html"
breadcrumb-title: ''
description: Aprenda a optimizar la configuración del hardware y la preparación de mallas para lograr un rendimiento de panificación más rápido.
helpx_creative_field: ""
helpx_description: bakers > Guides > Performances and optimizations
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rendimiento y optimizaciones
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---


# Rendimiento y optimizaciones

## Requisitos mínimos de hardware

No hay requisitos mínimos para usar Substance Bakers, sin embargo, es importante tener en cuenta lo siguiente:

* Una buena CPU ofrecerá tiempos de cálculo reducidos (múltiples núcleos acelerarán el cálculo de **desde panaderos de malla** que usan trazado de rayos).
* Una cantidad decente de memoria (RAM) permitirá cargar mallas con muchos detalles (polígonos).
* Una buena GPU te permitirá generar texturas con grandes resoluciones (como 8K).

## Triangulación

Los panaderos trabajan internamente con mallas trianguladas; si los modelos 3D (poly alta y baja) no se triangulan, los panaderos triangularán las mallas por sí mismos. Este proceso puede tomar mucho tiempo y se incrementará linealmente en relación con la cantidad de polígonos contenidos en el modelo. Por lo general, se recomienda triangular las mallas (especialmente la malla de polietileno alta) para evitar que este proceso se produzca durante la cocción.

Si el flujo de trabajo se basa en FBX, puede triangular la malla en el tiempo de exportación mediante una opción de la aplicación DCC.

## Caché de geometría

Consulte la siguiente página para obtener más información : [Caché de geometría](../../features/geometry-cache/geometry-cache.md)

## Suavizado

Los panaderos pueden utilizar un muestreo súper para realizar el suavizado. El supermuestreo significa que los panaderos emitirán más rayos por píxel para suavizar el resultado. El tiempo de cocción se puede ver dramáticamente afectado por este ajuste; esto es particularmente cierto para los panaderos donde se requieren muchos rayos, como la oclusión ambiental de mesh baker.

A modo de ejemplo:

* un ajuste AA de 2x2 significa que el panadero lanzará 4 veces la cantidad inicial de rayos. Para una textura de 2048\*2048 px, el cálculo resultante equivale a hornear una textura de 4096\*4096px y debería tardar unas 4 veces más en calcularse.
* un ajuste AA de 8x8 significa que el panadero lanzará 64 veces la cantidad inicial de rayos. Para una textura de 2048\*2048 px, el tiempo de cálculo resultante equivale a hornear una textura de 16384\*16384px y debería tardar unas 64 veces más en realizar el cálculo.

**Teniendo en cuenta estos números, la configuración 8x8 debe usarse con cuidado**.

Con el fin de reducir la presencia de ruido, generalmente se recomienda aumentar el número de rayos secundarios (para la oclusión ambiente, thickness y panaderos normales doblados) y mantener un ajuste 2x2 o 4x4 AA en lugar de utilizar una cantidad baja de rayos secundarios y un ajuste AA alto.

>[!NOTE]
>
> Un buen ajuste de rendimiento/calidad para la oclusión ambiental desde malla es usar AA 2x2 y al menos 128 rayos secundarios.

## Formato de archivo

La exportación de archivos en disco puede tardar bastante tiempo según el formato de archivo, la resolución, la profundidad de bits y la configuración de compresión. Los ajustes de compresión se pueden modificar en las opciones Preferencias / Proyectos / General / Formato de archivo. Al deshabilitar la compresión, se puede reducir el tiempo de exportación en la expansión de archivos más grandes.

## Bloqueos y TDR

Los bloqueos pueden deberse a varios factores, uno de los cuales es el TDR (Timeout Detection Recovery). El TDR es un mecanismo de Windows creado para detectar y recuperarse de situaciones en las que la GPU parece no responder. Debido a un valor predeterminado bajo para la detección de retardo TDR, se pueden producir bloqueos al utilizar panaderos específicos en algunas situaciones:

* al hornear mallas densas con el panadero de Oclusión Ambient
* al utilizar los panaderos acelerados DXR con mallas de polietileno muy densas (más de 60 millones de triángulos)

Puede encontrar información adicional sobre el TDR y una guía paso a paso sobre cómo puede modificar sus configuraciones asociadas aquí: [Los controladores de la GPU se bloquean con cálculos largos (bloqueo de TDR)](https://helpx.adobe.com/es/substance-3d/unlisted/documentation/spdoc/gpu-drivers-crash-with-long-computations-128745489.html)
