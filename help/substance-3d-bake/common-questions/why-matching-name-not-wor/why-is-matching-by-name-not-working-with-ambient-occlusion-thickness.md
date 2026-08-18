---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/common-questions/why-is-matching-by-name-not-working-with-ambient-occlusion-thickness.html"
breadcrumb-title: ''
description: Entiende por qué la coincidencia por nombre no funciona con los panaderos de Oclusión ambiental y Thickness, y encuentra alternativas.
helpx_creative_field: ""
helpx_description: "bakers > Common Questions > Why is Matching by Name not working with Ambient OcclusionThickness "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: '¿Por qué la coincidencia por nombre no funciona con el grosor de oclusión ambiental? '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# ¿Por qué la asociación por nombre no funciona con la Oclusión o el Thickness de ambiente?

>[!WARNING]
>
> **Pregunta**
> 
> He habilitado [Coincidencia por nombre](../../features/matching-by-name/matching-by-name.md) en los [parámetros comunes](../../bakers-settings/common-parameters/common-parameters.md) para filtrar y ordenar mis mallas de poli altas y bajas, ¿por qué el panadero de Oclusiones ambientales la ignora?

>[!NOTE]
>
> **Explicación**
> 
> Los rayos secundarios de lanzamiento de los panaderos Oclusión ambiental, Thickness y Normales dobladas se calculan al calcular sus texturas. Estos rayos tienen su propio ajuste de coincidencia por nombre.

>[!NOTE]
>
> **Solución : Substance Painter**
> 
> Solución: habilite el filtrado de coincidencia por nombre para los rayos secundarios en los parámetros de baker.
