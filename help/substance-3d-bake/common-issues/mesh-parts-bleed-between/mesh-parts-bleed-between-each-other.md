---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/common-issues/mesh-parts-bleed-between-each-other.html"
breadcrumb-title: ''
description: Evite que las partes de la malla se sangren entre sí durante el proceso de cocción, utilizando Coincidencia por nombre o ajustando las distancias.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Mesh parts bleed between each other
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Las partes de la malla se sangran entre sí
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# Las partes de la malla se sangran entre sí

>[!WARNING]
>
> **Problema**
> 
> La geometría de malla se purga en otras partes y crea artefactos.
> 
> ![](../../assets/bleed-example.png)

>[!NOTE]
>
> **Explicación**
> 
> El proceso de cocción envía rayos desde la superficie de la malla de bajo contenido de poli para golpear la malla de alto contenido de poli y crear una coincidencia. A veces los rayos van demasiado lejos y golpean la geometría equivocada, creando la hemorragia y artefactos.

>[!NOTE]
>
> **Solución**
> 
> Hay disponibles algunas soluciones para evitar este problema :
> 
> * Utilice la característica [Coincidencia por nombre](../../features/matching-by-name/matching-by-name.md) para aislar las mallas
> * Use una [jaula](https://helpx.adobe.com/es/substance-3d/unlisted/documentation/bake/cage-projection-172822982.html) para limitar la distancia del rayo.
> * Cambie la distancia de rayo predeterminada en los ajustes comunes del panadero a un valor inferior.
