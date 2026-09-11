---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/renderers/corona.html"
breadcrumb-title: ''
description: Utilice materiales de Substance con el procesador Corona en 3ds Max mediante el flujo de trabajo Specular/Brillo y los mapas necesarios.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Corona
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Corona
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 1%

---


# Corona

Para el renderizado con Corona puede utilizar mapas exportados desde Substance Painter o el plugin de Substance. Corona utiliza el flujo de trabajo Specular/Brillo con un mapa 1/IOR. Necesitará los siguientes mapas:

* Difusión
* Reflejo (Specular)
* Brillo
* 1/IOR (Convertido)

El mapa 1/IOR solo se puede convertir a partir del flujo de trabajo metálico/rugosidad, que es el flujo de trabajo predeterminado tanto en Substance Designer como en Substance Painter.

1. Exporte mapas de Substance Painter con el ajuste preestablecido Corona.
1. Para los Substance personalizados, puede utilizar el nodo convertido basecolor\_metallic\_roughness establecido en el ajuste preestablecido Vray para crear las salidas personalizadas.
1. Para 3ds Max y Cinema 4D, se utiliza un material de Corona en capas para manipular materiales metálicos y dieléctricos y evitar la necesidad de convertir un mapa 1/IOR.

## Tabla de contenido

* [Corona para 3ds Max](../../renderers/corona/corona-for-3ds-max/corona-for-3ds-max.md)
* [Corona - Substance Painter](../../renderers/corona/corona-painter/corona-substance-painter.md)
