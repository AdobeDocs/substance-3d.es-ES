---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/renderers.html"
breadcrumb-title: ''
description: Utiliza materiales Substance con renderizadores importantes como Arnold, V-Ray, Redshift y otros en tu flujo de trabajo 3D.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Renderizadores
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---


# Renderizadores

Los materiales de Substance proporcionados en [Substance Source](https://source.substance3d.com/) contienen salidas para sombreadores basados físicamente y admiten los flujos de trabajo [Metallic/Roughness (flujo de trabajo predeterminado) y Specular/Glossiness](https://academy.substance3d.com/courses/pbrguides). Es importante conocer el flujo de trabajo que admite el material del procesador. En función del procesador, es posible que pueda utilizar salidas de material de Substance directamente o que necesite convertir las texturas de salida. Es posible que los materiales de Substance personalizados o los materiales que descargue de Substance share no contengan los resultados adecuados necesarios para un procesador determinado.

![](../assets/outputs.png){width="200px"}

Por ejemplo, con Arnold o Vray Next, puede utilizar salidas metálicas/de rugosidad directamente. Sin embargo, con pxrSurface de Renderman, las salidas de color/metálico base deben convertirse a color difuso y de cara de specular. Un plugin de integración de Substance gestionará estas conversiones automáticamente si el procesador es compatible.

Con Substance Painter, puedes elegir una [Plantilla de salida](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/getting-started/export/export-window/export-window) que creará los tipos de mapa apropiados necesarios para un procesador determinado. Si el procesador no es compatible de forma predeterminada, también puede crear Plantillas de salida personalizadas.

**Plantilla de salida del Substance Painter**

![](../assets/output-template.png){width="500px"}

## Guías de procesador

* [Conversión de salidas de Substance](../renderers/converting-outputs/converting-substance-outputs.md)
* [Gestión de colores](../renderers/color-management/color-management.md)
* [Arnold](../renderers/arnold/arnold.md)
* [Variar](../renderers/vray/vray.md)
* [Renderman](../renderers/renderman/renderman.md)
* [Redshift](../renderers/redshift/redshift.md)
* [Maxwell](../renderers/maxwell/maxwell.md)
* [Corona](../renderers/corona/corona.md)
* [Octano](../renderers/octane/octane.md)
* [Keyshot](../renderers/keyshot/keyshot.md)
* [Thea](../renderers/thea/thea.md)
* [Maverick](../renderers/maverick/maverick.md)
* [Toolbag](../renderers/toolbag/toolbag.md)
* [Ciclos y pares](../renderers/cycles-and-eevee/cycles-and-eevee.md)
