---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/bakers-settings/color-map-from-mesh.html"
breadcrumb-title: ''
description: Proyecte propiedades de color desde mallas de alta densidad de poli en texturas para hornear ID de polipintura o material para máscaras de selección.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Color Map from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mapa de colores de malla
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 4%

---


# Mapa de colores de malla

Este mapa de color de mesh baker proyecta las propiedades de color de una malla de alta definición en una textura. Se puede utilizar para hornear ID de pintura o de material para crear máscaras de selección.

**Disponible en:**

* Substance Designer
* Substance Automation Toolkit
* Substance Painter

## Parámetros

| *Parámetro* | *Descripción* |
| --- | --- |
| **Origen de color** | Controla en qué propiedad de la malla de alta densidad debe basarse la generación de color.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Color de vértice</strong>: lee el color del vértice y guárdelo en la textura. Los colores se interpolan de un vértice a otro.</li><li data-preserve-html="true"><strong>Color de material</strong>: lee el color de material asignado a una cara de polígono.</li><li data-preserve-html="true"><strong>Id. de malla</strong>: asignar un color por cada objeto encontrado.</li><li data-preserve-html="true"><strong>Id. de grupo/submalla</strong>: asignar un color por subobjeto (también denominado elemento).</li></ul> |
| **Generador de colores** | Define cómo se genera el color cuando el **Origen de color** se establece en **ID de malla** o **ID de grupo o submalla**. Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Aleatorio</strong>: cada objeto o subobjeto tiene un color generado aleatoriamente.</li><li data-preserve-html="true"><strong>Cambio de tono</strong>: cada objeto o subobjeto tiene un color único basado en un tono.</li><li data-preserve-html="true"><strong>Escala de grises</strong>: cada objeto o subobjeto presenta un color con un valor de escala de grises único.</li></ul> |
