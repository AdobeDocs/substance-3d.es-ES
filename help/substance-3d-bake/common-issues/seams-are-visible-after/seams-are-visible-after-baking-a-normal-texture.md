---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-issues/seams-are-visible-after-baking-a-normal-texture.html"
breadcrumb-title: ''
description: Elimina las costuras visibles en texturas normales horneadas ajustando el relleno, el suavizado y el diseño UV.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Seams are visible after baking a normal texture
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Las costuras son visibles después de hornear una textura normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---


# Las costuras son visibles después de hornear una textura normal

>[!WARNING]
>
> **Problema**
> 
> Las costuras normales del mapa son visibles en los bordes UV de la malla incluso después de una cocción limpia.

>[!NOTE]
>
> **Explicación**
> 
> Incluso después de una cocción perfecta, las costuras todavía pueden ser visibles. La razón principal es que una superficie normal aproxima la información en una textura. A veces la textura carece de precisión o tiene que compensar demasiado entre la geometría de poli baja y alta para ser lo suficientemente precisa. En otra situación, la forma en que se licita la geometría con su mapa normal puede afectar su aspecto.

>[!NOTE]
>
> **Solución**
> 
> Se pueden intentar algunas soluciones posibles para reducir la intensidad de las costuras con mapas normales:
> 
> * A menudo, las coordenadas UV no se alinean con los píxeles, lo que provoca un suavizado y produce costuras. Consulte [esta página](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md) para obtener más información.
>   * Aumentar la resolución de la textura puede ser una forma de reducir este efecto.
>   * Alinear los bordes UV a píxeles es otra forma de reducir este efecto.
> * Aumente la configuración del sombreador **quality**. La calidad del sombreado puede afectar al modo en que se calculan los reflejos del specular. Si se rotan algunas Islas de UV y este parámetro es demasiado bajo, puede producir costuras visibles. Consulte [esta página](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/pbr-metal-rough-172818827.html) para obtener más información.
