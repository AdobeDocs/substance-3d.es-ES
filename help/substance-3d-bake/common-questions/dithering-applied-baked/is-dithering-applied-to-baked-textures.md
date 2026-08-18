---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/common-questions/is-dithering-applied-to-baked-textures.html"
breadcrumb-title: ''
description: Obtenga información sobre si el tramado se aplica a texturas al horno y cómo afecta a la calidad de la textura.
helpx_creative_field: ""
helpx_description: "bakers > Common Questions > Is dithering applied to baked textures "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: '¿Se aplica el tramado a las texturas horneadas? '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---


# ¿Se aplica el tramado a las texturas al horno?

>[!WARNING]
>
> **Pregunta**
> 
> ¿Admite los panaderos el tramado de textura [y, si es así, cuándo se aplica?](https://en.wikipedia.org/wiki/Dither)

>[!NOTE]
>
> **Explicación**
> 
> El tramado se aplica para evitar bandas en mapas normales de 8 bits, por ejemplo:
> 
> ![](../../assets/dither.jpg)

>[!NOTE]
>
> **Solución : Substance Designer**
> 
> El tramado se aplica automáticamente en las siguientes situaciones:
> 
> * Cuando se guarda una salida de Baker en un archivo de textura de 8 bits
> * Cuando se utiliza una salida de Baker en un nodo de mapa de bits de un gráfico definido en 8 bits.

>[!NOTE]
>
> **Solución : Substance Painter**
> 
> El tramado es una opción que se puede activar o desactivar durante el proceso de exportación. Solo se aplica al exportar a formato de archivo de 8 bits para los canales Normal, Desplazamiento y Height.

>[!NOTE]
>
> **Solución : Kit de herramientas de automatización de Substance**
> 
> Por el momento, no se admite el tramado.
