---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/common-questions/should-i-enable-compute-tangent-space-per-fragment.html"
breadcrumb-title: ''
description: Obtenga información sobre cuándo activar Calcular espacio tangente por fragmento y cómo afecta a los resultados de hacer un bake.
helpx_creative_field: ""
helpx_description: bakers > Common Questions > Should I enable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ¿Debo habilitar
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 1%

---


# ¿Se debe activar Calcular el espacio tangente por fragmento?

>[!WARNING]
>
> **Pregunta**
> 
> ¿Qué significa la configuración &quot;Calcular espacio tangente por fragmento&quot; y para qué se utiliza?

>[!NOTE]
>
> **Explicación**
> 
> Cuando esta opción está activada, indica al baker que realice el cálculo del Espacio de tangente en el Sombreador de fragmentos (también denominado Sombreador de píxeles) en lugar del Sombreador de vértices. Lo que significa que el cálculo se realizará por píxel en lugar de interpolarse de un vértice a otro. El baker de mapa de normales utiliza esta configuración para saber cómo codificar la textura. También solía saber cómo leer la textura de los sombreadores.
> 
> Para activar o desactivar este parámetro, normalmente es necesario volver a realizar las texturas para sincronizarlas con las ventanas gráficas 3D y los motores de procesamiento (como Iray).

>[!NOTE]
>
> **Solución**
> 
> Dependiendo del software o motor de juegos que se vaya a procesar para la textura, esta configuración puede estar deshabilitada o habilitada:
> 
> | *Software* | *Calcular espacio tangente por fragmento* |
> | --- | --- |
> | **Motor irreal 4** | Activado |
> | **Unidad** | Desactivado |
