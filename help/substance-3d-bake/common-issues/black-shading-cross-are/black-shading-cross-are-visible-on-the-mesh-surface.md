---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/black-shading-cross-are-visible-on-the-mesh-surface.html"
breadcrumb-title: ''
description: Corrija los defectos de sombreado negro visibles en las superficies de malla corrigiendo el espacio tangente y los cálculos normales.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Black shading cross are visible on the mesh surface
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Las cruces de sombreado negro son visibles en la superficie de la malla
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---


# La cruz de sombreado negro es visible en la superficie de la malla

Aparecen defectos de sombreado negro en varias áreas de la malla bajo iluminación.

![](../../assets/black-shading-cross.jpg)


## Explicación

Una cruz sombreada en negro normalmente significa que el mapa normal no coincide con la malla, generalmente porque la geometría de la malla ha cambiado o se ha calculado de una manera diferente al cálculo realizado por el panadero. Por ejemplo: la triangulación de la malla es diferente entre el panadero y la ventana gráfica que representa la malla y su mapa normal.

## Solución

Asegúrese de que la aplicación que muestra la malla y su mapa normal se sincroniza con la forma en que se ha horneado la textura. Esto implica:

* Compruebe que el espacio tangente sea idéntico entre el espectador y el panadero.
* Compruebe que el formato Normal es idéntico entre la vista y el panadero.
* Verificar que la Triangulación sea idéntica entre el espectador y el panadero. Consulte [esta página](../../guides/triangulating-before-bak/triangulating-before-baking.md) para obtener más información.
