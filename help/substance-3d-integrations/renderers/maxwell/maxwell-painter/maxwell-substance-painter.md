---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/renderers/maxwell/maxwell-substance-painter.html"
breadcrumb-title: ''
description: Exporte texturas de Substance Painter para el procesador de Maxwell utilizando las plantillas de salida y los ajustes de materiales adecuados.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Maxwell > Maxwell - Substance Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maxwell - Substance Painter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# Maxwell - Substance Painter

Substance Painter 2020.1 (6.1.0) admite las [Plantillas de salida](https://experienceleague.adobe.com/es/docs/substance-3d-painter/using/getting-started/export/export) de Maxwell en lo que respecta a los elementos metálicos/rugosos y a los speculares/brillantes. Simplemente puede exportar utilizando la Plantilla de salida Maxwell**.\
Maxwell 5.1.0** tiene una integración con Substance Painter que le permite importar fácilmente texturas y configurar automáticamente un material de Maxwell.

## Exportación de texturas

Puede elegir las Plantillas de salida Maxwell (Rugosidad metálica) o Maxwell (Brillo de Specular) para exportar texturas y procesarlas en Maxwell.

![](../../../assets/maxwell-output.png){width="500px"}

## Aplicación de texturas en Maxwell

Puede utilizar la integración de Substance Painter en Maxwell para crear automáticamente un material con los mapas exportados de Substance Painter aplicados.\
Para empezar, haz clic con el botón derecho en la Lista de materiales y elige **Nuevo>Substance Painter**.

![](https://helpx-prod.scene7.com/is/image/HelpxProd/maxwell-painter?$png$&jpegSize=100&wid=413)

Vaya a la ubicación donde haya exportado las texturas de Substance Painter y seleccione uno de los mapas, como el color base. Al hacer clic en abrir, la integración creará un nuevo material de Maxwell con los mapas asignados.\
Si tiene varios conjuntos de texturas exportados desde Substance Painter, la integración utilizará la convención de nomenclatura de la textura para asignar los mapas de textura coincidentes.

![](https://helpx-prod.scene7.com/is/image/HelpxProd/image-material?$png$&jpegSize=100&wid=620){width="600px"}

A continuación, puede asignar el material al activo de la escena.

![](../../../assets/assigned.png){width="500px"}

Todos los materiales se aplican mediante la integración de Substance Painter.

![](https://helpx-prod.scene7.com/is/image/HelpxProd/materials-assigned?$pjpeg$&jpegSize=300&wid=1511){width="800px"}
