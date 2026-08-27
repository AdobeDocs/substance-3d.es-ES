---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/aliasing-on-uv-seams.html"
breadcrumb-title: ''
description: Corrija los artefactos de suavizado que aparecen en las costuras UV durante el horneado ajustando los ajustes de suavizado y relleno.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Aliasing on UV Seams
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Suavizado en costuras UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---


# Suavizado en costuras UV

>[!WARNING]
>
> **Problema**
> 
> Aparecen puntos o manchas oscuros en el borde de las costuras UV después de hornear:
> 
> ![](../../assets/edge-aliasing.png)

>[!NOTE]
>
> **Explicación**
> 
> Cuando el Baker anota información en la textura, tiene que convertirse de geometría a píxeles. El procesamiento de esta información puede introducir [alias](https://en.wikipedia.org/wiki/Aliasing). El suavizado suele producirse porque la geometría de las coordenadas UV no está alineada con la cuadrícula de píxeles o porque las coordenadas UV no cubren suficientes píxeles para proporcionar una resolución suficiente.
> 
> En las siguientes imágenes, la geometría es la superposición roja. El panadero marcará un píxel como lleno si la geometría cubre más de la mitad de su superficie (los cuadrados blancos son píxeles completos y los cuadrados negros son píxeles vacíos). En la imagen de la derecha, la cuadrícula de píxeles tiene el doble de resolución, lo que permite una representación más precisa de la geometría.
> 
> ![](../../assets/aliasing-example-large.png)
> 
> ![](../../assets/aliasing-example-small.png)

>[!NOTE]
>
> **Solución**
> 
> * Aumente la resolución de textura de salida de los Bakers.
> * Aumente el ajuste de suavizado (nota : puede tardar más tiempo en calcularse).
> * Alinee las coordenadas UV con la cuadrícula de píxeles en el editor UV del software de modelado 3D.
> * Proporcione una mejor proporción de texto respecto a los UV.
