---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/renderers/arnold/arnold-substance-painter.html"
breadcrumb-title: ''
description: Utilice las plantillas de salida de Substance Painter para el procesador de Arnold con material de aiStandard para el procesamiento basado en la física.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Arnold > Arnold - Substance Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Arnold - Substance Painter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---


# Arnold - Substance Painter

Substance Painter 2020.1 (6.1.0) se envía con [Plantillas de salida](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/getting-started/export/output-templates/export-presets) para Arnold mediante el [material aiStandard](https://docs.arnoldrenderer.com/display/A5AFMUG/Standard+Surface).

![](../../../assets/arnold-export.png){width="800px"}

## Sombreador Arnold Standard (Arnold 5 y superior)

| Exportación de Substance Painter | Arnold AiStandardSurface |
| --- | --- |
| BaseColor | Base/color |
| Rugosidad | Specular / Rugosidad |
| Metalicidad | Base / Metalness |
| Normal | (**Maya**) Geometría/ Asignación de relieve / bump2d (Utilizar como normales de espacio tangente) (**3ds** **Max**) Mapa de bits → Normal |
| Altura | (**Maya**) Sombreador de Desplazamiento / desplazamiento (**3ds** **Max**) Modificador de objeto → Propiedades de Arnold → Desplazamiento → Usar mapa |
| Emisivo | Emisión/ Color (Peso De Emisión = 1,0) |
| Nivel de anisotropía (no incluido en la Plantilla de salida Arnold predeterminada) | (**Maya**) Abrigo/ Anisotropía (**3ds** **Max**) Abrigo/ Anisotropía |
| Nivel de anisotropía (no incluido en la Plantilla de salida Arnold predeterminada) | (**Maya**) Abrigo/ Rotación (**3ds** **Max**) Abrigo/ Rotación |

>[!NOTE]
>
> Los mapas que representan datos deberán interpretarse correctamente. Para obtener más información, consulta la página [Administración de color](../../../renderers/color-management/color-management.md).
