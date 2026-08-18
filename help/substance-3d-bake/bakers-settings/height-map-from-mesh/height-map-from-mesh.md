---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/bakers-settings/height-map-from-mesh.html"
breadcrumb-title: ''
description: Cree mapas de height a partir de mallas de alto contenido poliéster para capturar los detalles de la superficie y la información de geometría para el texturizado.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Height Map from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mapa de altura de malla
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 8%

---


# Mapa de altura de malla

El mapa de Height de mesh baker le permite crear un mapa de height a partir de una malla de poli alta.**Disponible en:**

* Painter
* Designer
* Automation Toolkit

## Parámetros

| *Parámetro* | *Descripción* |
| --- | --- |
| **&#x200B;**&#x200B;Normalización&#x200B;**&#x200B;** | Define cómo se debe guardar el rango de valores de height en la textura.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Relativo a la distancia de rayos</strong>:</li><li data-preserve-html="true"><strong>Relativo a malla de poli baja (por azulejo UV)</strong> (predeterminado)</li><li data-preserve-html="true"><strong>Relativo a mín./máx. (por mosaico UV)</strong></li><li data-preserve-html="true"><strong>Manual</strong></li></ul> |
| **Divisor de escala** | Defina cuánto deben multiplicarse o dividirse los valores de height.Solo está disponible cuando **Normalization** está establecido en **Manual**. |
