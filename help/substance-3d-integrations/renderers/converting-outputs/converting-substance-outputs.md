---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/renderers/converting-substance-outputs.html"
breadcrumb-title: ''
description: Aprenda a convertir las salidas de material de Substance para que coincidan con los diferentes requisitos y flujos de trabajo del procesador.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Converting Substance outputs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Conversión de salidas de Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---


# Conversión de salidas de Substance

## Substance Painter

Puede exportar los mapas convertidos desde Substance Painter. Se admite una amplia gama de ajustes preestablecidos de procesamiento y, si selecciona un ajuste preestablecido, se convertirán los tipos de mapas. (la conversión se basa en el flujo de trabajo de metal/desbaste).

![](../../assets/convertpainter.png){width="800px"}

## Complemento de Substance

El complemento Substance generará salidas y creará automáticamente materiales para flujos de trabajo específicos. Sin embargo, con las aplicaciones de DCC y los procesadores de terceros, puede que necesite convertir manualmente las salidas metálicas/iniciales. Las siguientes integraciones admiten flujos de trabajo de representación automática y convertirán adecuadamente cualquier tipo de mapa si es necesario:

* [Substance en Maya](../../3d-applications/maya/using-workflows/using-workflows.md)
* [Substance en 3ds Max](../../3d-applications/3ds-max/3ds-max.md)

## Substance personalizados

Si está creando un Substance personalizado, puede crear las salidas específicas que necesita para los procesadores como Vray y Corona. Mediante el nodo de conversión de metal/rugosidad (Biblioteca>Utilidades PBR), puede convertir fácilmente los mapas de color base, rugosidad y metálicos al procesador específico.

![](../../assets/convert-designer.png){width="600px"}
