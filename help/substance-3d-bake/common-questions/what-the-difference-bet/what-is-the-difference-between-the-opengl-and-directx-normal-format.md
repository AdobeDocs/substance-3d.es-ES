---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-questions/what-is-the-difference-between-the-opengl-and-directx-normal-format.html"
breadcrumb-title: ''
description: Conozca las diferencias entre OpenGL y los formatos de mapa de normales de DirectX y cuándo usar cada uno.
helpx_creative_field: ""
helpx_description: "bakers > Common Questions > What is the difference between the OpenGL and DirectX normal format "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: '¿Cuál es la diferencia entre el formato normal de OpenGL y DirectX? '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---


# ¿Cuál es la diferencia entre el formato normal de OpenGL y DirectX?

>[!WARNING]
>
> **Pregunta**
> 
> ¿Cuál es la diferencia entre el formato normal de OpenGL y DirectX?

>[!NOTE]
>
> **Explicación**
> 
> OpenGL y DirectX son dos API gráficas (conjuntos de funciones) que los programadores utilizan en su aplicación para dialogar con la GPU (unidad de procesamiento gráfico). En términos de mapas normales, la diferencia resulta en cómo debe interpretarse el canal verde de una textura RGB. OpenGL espera que el primer píxel esté en la parte inferior, mientras que el DirectX espera que esté en la parte superior. Esto es a menudo por lo que en varias discusiones técnicas se recomienda tratar de invertir el canal verde de un mapa normal para ver si se comporta mejor ya que invierte los valores de píxeles (primero se convierte en último). OpenGL se puede referir como **Y+** (ascendente), mientras que el DirectX se refiere como **Y-** (descendente).
> 
> Para saber qué formato utilizar, consulte la aplicación de destino en la que se utilizarán las texturas.
