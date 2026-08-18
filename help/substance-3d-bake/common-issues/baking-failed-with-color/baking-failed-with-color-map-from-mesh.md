---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/common-issues/baking-failed-with-color-map-from-mesh.html"
breadcrumb-title: ''
description: Resuelva los errores de asignación de color de los errores de asignación de malla comprobando las propiedades de color de la malla y la asignación de UV.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Baking failed with Color Map from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Error de procesamiento con asignación de color desde malla
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---


# Error de procesamiento con asignación de color desde malla

>[!WARNING]
>
> **Problema**
> 
> Posible mensaje de error:
> 
> &#x200B;> > > 
> 
> Error de cocción (mapa de color de la malla)\
> No se han encontrado colores de vértice

>[!NOTE]
>
> **Explicación**
> 
> La configuración predeterminada para el [Mapa de color de malla](../../bakers-settings/color-map-from-mesh/color-map-from-mesh.md) es convertir los colores del vértice de malla de alta densidad en una textura basada en las UV de malla. Sin embargo, a menudo ocurre cuando la malla de alta densidad no tiene ninguna información de colores de vértice. Por lo tanto, el panadero no puede escribir información que no existe.

>[!NOTE]
>
> **Solución**
> 
> Existen diferentes soluciones para evitar este mensaje de error:
> 
> * Utilice una malla de alta densidad que tenga colores de vértice
> * Definir el mapa de color desde el panadero de malla con diferentes ajustes
> * No utilice el Mapa de color de Mesh Baker si no lo necesita
