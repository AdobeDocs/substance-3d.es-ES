---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/common-issues/normal-texture-looks-faceted.html"
breadcrumb-title: ''
description: Corrige el aspecto facetado en texturas normales suavizando las normales de malla y ajustando los ajustes de suavizado de grupos.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Normal texture looks faceted
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: La textura normal parece faceteada
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# La textura normal parece faceteada

>[!WARNING]
>
> **Problema**
> 
> La textura Normal tiene un aspecto facetado o cada cara de la malla es visible en ella después de hornearla.
> 
> ![](../../assets/normal-faceted.jpg)

>[!NOTE]
>
> **Explicación**
> 
> La razón principal por la que la cocción de una normal produciría este resultado es porque las normales de malla de poli baja no se establecen correctamente. Cada borde de cada cara es un borde duro, haciendo que la proyección de rayos durante el emparejamiento con la malla de alta polietileno ignore la información de los vecinos y cree costuras o información inconsciente. Si bien el resultado puede verse bien en la malla, esto puede llevar a problemas de sombreado más adelante y debe resolverse.

>[!NOTE]
>
> **Solución**
> 
> La solución principal es retrabajar el vértice normal o la malla de polietileno bajo, la denominación exacta del proceso depende del software de modelado 3D:
> 
> * Usa **normales promedio** en Maya, Houdini.
> * Usar **un grupo de suavizado** en 3DS Max.
> * Use **sombreado suave** en Blender.
> * Las mallas exportadas desde zBrush siempre tendrán facetas y se deben limpiar en otro software.
> 
> Tenga en cuenta que esto puede no ser suficiente: asegúrese de que los ajustes también guarden/generen la información normal o de sombreado del vértice al exportar una malla.
