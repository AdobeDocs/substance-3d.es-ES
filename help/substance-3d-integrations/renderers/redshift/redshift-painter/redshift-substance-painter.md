---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/renderers/redshift/redshift-substance-painter.html"
breadcrumb-title: ''
description: Exporte texturas de Substance Painter para el procesador Redshift mediante plantillas de salida y ajustes de material adecuados.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Redshift > Redshift - Substance Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cambio de rojo - Substance Painter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# Cambio de rojo - Substance Painter

Substance Painter 2020.1 (6.1.0) admite Redshift [Plantillas de salida](https://docs.substance3d.com/display/SPDOC/Export) para metales/rugosidad (rsMaterial). Simplemente puede exportar utilizando la plantilla Redshift para producir texturas que sean compatibles con los materiales Redshift.

![](../../../assets/rs-export.png)

## Configuración de material de Redshift

| Exportación de Substance Painter | Material de desplazamiento al rojo |
| --- | --- |
| Color | Difusión / Color |
| Rugosidad | Reflejo / Rugosidad (BRDF = GGX) |
| Metalicidad | Reflejo / Metalness (Fresnel Type = Metalness) |
| Normal | Global / Mapa de relieve / rsBumpMap (Tipo de mapa de entrada = Espacio tangente normal - Escala de Height = 1.0) |
| DesplazarCampoAlto | Sombreador de desplazamientos / rsAsignación de texto de desplazamiento (codificación de mapa = campo de Height) |
| EmissionColor | Total / Emisión (Peso De Emisión = 1,0) |

>[!NOTE]
>
> Los mapas que representan datos deberán interpretarse correctamente. Para obtener más información, consulta la página [Administración de color](../../../renderers/color-management/color-management.md).

## Ejemplo de Maya/Redshift

![](https://helpx-prod.scene7.com/is/image/HelpxProd/maya-example?$pjpeg$&jpegSize=300&wid=1583){width="800px"}
