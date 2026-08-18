---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/renderers/renderman/renderman-substance-painter.html"
breadcrumb-title: ''
description: Exporte texturas Substance Painter para Renderman utilizando material pxrSurface y conversiones de salida adecuadas.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Renderman > Renderman - Substance Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Renderman - Substance Painter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 1%

---


# Renderman - Substance Painter

Substance Painter 2020.1 (6.1.0) admite [**pxrSurface**](https://rmanwiki.pixar.com/display/REN/PxrSurface) y [Plantillas de salida](https://docs.substance3d.com/display/SPDOC/Export) de pxrDisney.

![](../../../assets/renderman.png)

Se recomienda usar **pxrSurface** para el resultado.

![](../../../assets/pxrsurface.png)

## Renderman Shader (Maya - RM 23.1)

| Exportación de Substance Painter | PxrSurface |
| --- | --- |
| DiffuseColor | Difusión / Color |
| RugosidadEspecular | Specular principal / Rugosidad |
| SpecularFaceColor | Specular principal / Color de la cara |
| Normal | Globales / Rugosidad / PxrNormalMap → Orientación (Open GL) |
| Desplazamiento | (canal rojo) PxrDispTransform (Resultado F) → (disp escalar) PxrDisplace (Color de salida) → (Sombreado de Desplazamiento) PxrSurfaceSG |
| GlowColor | Resplandor/Color (ganancia = 1,0) |
| Presencia | Globales / Presencia |

>[!NOTE]
>
> Los mapas que representan datos deberán interpretarse correctamente. Para obtener más información, consulta la página [Administración de color](../../../renderers/color-management/color-management.md).
