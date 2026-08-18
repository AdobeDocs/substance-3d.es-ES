---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/seam-visible-on-every-face.html"
breadcrumb-title: ''
description: Corrija las costuras visibles en cada cara comprobando el desajuste de UV, los grupos de suavizado y los problemas de topología de malla.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Seam visible on every face
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Costura visible en cada cara
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Costura visible en cada cara

>[!WARNING]
>
> **Problema**
> 
> Se puede ver una costura en algunos bordes de la geometría aunque no haya costuras UV:
> 
> ![](../../assets/seam-every-face.jpg)

>[!NOTE]
>
> **Explicación**
> 
> Si no se usa una [jaula](https://helpx.adobe.com/substance-3d/unlisted/documentation/bake/cage-projection-172822982.html), el proceso de horneado iniciará rayos en la dirección de los vértices normales de la malla de baja densidad. Si cada vértice normal está dividido (lo que significa que cada cara no comparte los mismos vértices normales que la cara vecina), los rayos no se enviarán en la misma dirección en los bordes. Esto da como resultado la división, ya que la información de cada lado de los bordes es diferente.
> 
> Este problema también se agrava por el suavizado, como se explica en [esta página](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md).

>[!NOTE]
>
> **Solución**
> 
> Aquí solo se pueden encontrar dos soluciones:
> 
> * Use una [jaula](https://helpx.adobe.com/substance-3d/unlisted/documentation/bake/cage-projection-172822982.html) para controlar la dirección del rayo en lugar de permitir que el panadero lo calcule a partir de la geometría de baja polea.
> * Combine los vértices normales de la malla de baja densidad (suavícelos o aplique un grupo de suavizado común).
