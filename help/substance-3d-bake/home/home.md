---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/home.html"
breadcrumb-title: ''
description: Aprende a usar Substance Bakers para calcular información basada en mallas en archivos de texturas y mejorar tu flujo de trabajo de texturas.
helpx_creative_field: ""
helpx_description: bakers > Home
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance Bakers
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 13%

---


# Substance Bakers

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<b>Substance Bakers</b> es un conjunto de herramientas de algoritmo avanzado para calcular información basada en mallas en archivos de texturas. Cualquier artista con una malla 3D puede utilizarlas para aprovechar los métodos avanzados de texturizado. La panificación es un proceso esencial en el flujo de trabajo del software de Substance para ofrecer <b> herramientas eficaces</b> y <b>texturas automatizadas</b>.

Esta documentación abarca los <b>aspectos fundamentales del procesamiento</b> y los <b>problemas comunes</b> y los errores que se pueden encontrar al tratar este proceso.

</td>
<td width="58.30%" style="border: 0;" valign="top">

![](../assets/optim-baker-home.png){width="400px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Procedimientos iniciales

* [¿Qué es el Baking?](../getting-started/what-is-baking/what-is-baking.md)
* Hornear con:
  * [Substance 3D Painter](../getting-started/software-interface/3d-painter/substance-3d-painter.md)
  * [Substance 3D Designer](../getting-started/software-interface/3d-designer/substance-3d-designer.md)
  * [Substance 3D Automation Toolkit](../getting-started/software-interface/3d-automation-toolkit/substance-3d-automation-toolkit.md)
* [Disponibilidad por software](../getting-started/availability-per-software/availability-per-software.md)
* [Software 3D compatible](../getting-started/compatible-3d-software/compatible-3d-software.md)
* [Tutoriales](../getting-started/tutorials/tutorials.md)

</td>
<td style="border: 0;" valign="top">

### Configuración de panaderos

* [Parámetros comunes](../bakers-settings/common-parameters/common-parameters.md)
* [Oclusión ambiental](../bakers-settings/ambient-occlusion/ambient-occlusion.md)
* [Oclusión ambiental desde malla](../bakers-settings/ambient-occlusion-from/ambient-occlusion-from-mesh.md)
* [Normales dobladas de la malla](../bakers-settings/bent-normals-from-mesh/bent-normals-from-mesh.md)
* [Mapa de colores de malla](../bakers-settings/color-map-from-mesh/color-map-from-mesh.md)
* [Convertir UV a SVG](../bakers-settings/convert-uv-to-svg/convert-uv-to-svg.md)
* [Curvatura](../bakers-settings/curvature/curvature.md)
* [Curvatura desde malla](../bakers-settings/curvature-from-mesh/curvature-from-mesh.md)
* [Curvatura desde malla (obsoleto)](../bakers-settings/curvature-from-mesh-dep/curvature-from-mesh-deprecated.md)
* [Mapa de altura de malla](../bakers-settings/height-map-from-mesh/height-map-from-mesh.md)
* [Mapa de normales de malla](../bakers-settings/normal-map-from-mesh/normal-map-from-mesh.md)
* [Máscara de opacidad de malla](../bakers-settings/opacity-mask-from-mesh/opacity-mask-from-mesh.md)
* [Posición](../bakers-settings/position/position.md)
* [Mapa de posición desde malla](../bakers-settings/position-map-from-mesh/position-map-from-mesh.md)
* [Mapa de grosor de malla](../bakers-settings/thickness-map-from-mesh/thickness-map-from-mesh.md)
* [Textura transferida de malla](../bakers-settings/transferred-texture-from/transferred-texture-from-mesh.md)
* [Dirección de espacio de mundo](../bakers-settings/world-space-direction/world-space-direction.md)
* [Normales de espacio de mundo](../bakers-settings/world-space-normals/world-space-normals.md)

</td>
<td style="border: 0;" valign="top">

### Guías

* [Mensajes de error y de advertencia](../guides/error-and-warning-mes/error-and-warning-messages.md)
* [Rendimiento y optimizaciones](../guides/performances-and-opt/performances-and-optimizations.md)
* [Triangulando antes de hornear](../guides/triangulating-before-bak/triangulating-before-baking.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Funciones

* [Caché de geometría](../features/geometry-cache/geometry-cache.md)
* [Trazado de rayos de GPU](../features/gpu-raytracing/gpu-raytracing.md)
* [Coincidencia por nombre](../features/matching-by-name/matching-by-name.md)
* [Espacio tangente](../features/tangent-space/tangent-space.md)

</td>
<td style="border: 0;" valign="top">

### Preguntas habituales

* [¿Cómo se exportan los mapas con bake?](../common-questions/how-export-the-baked-maps/how-to-export-the-baked-maps.md)
* [¿Se aplica el tramado a las texturas al horno?](../common-questions/dithering-applied-baked/is-dithering-applied-to-baked-textures.md)
* [¿Se debe activar Calcular el espacio tangente por fragmento?](../common-questions/should-enable-compute-tan/should-i-enable-compute-tangent-space-per-fragment.md)
* [La textura horneada fuera del software del Substance parece incorrecta](../common-questions/texture-baked-outside-sof/texture-baked-outside-of-substance-software-looks-incorrect.md)
* [¿Qué son los archivos Assbin?](../common-questions/what-are-assbin-files/what-are-assbin-files.md)
* [¿Cuál es la profundidad de bits de las texturas al horno?](../common-questions/what-the-bit-depth-baked/what-is-the-bit-depth-of-baked-textures.md)
* [¿Cuál es la diferencia entre el formato normal de OpenGL y DirectX?](../common-questions/what-the-difference-bet/what-is-the-difference-between-the-opengl-and-directx-normal-format.md)
* [¿Por qué hay extraños estiramientos en mis texturas después de hornear o exportar?](../common-questions/why-are-there-strange-str/why-are-there-strange-stretches-in-my-textures-after-baking-or-exporting.md)
* [¿Por qué la asociación por nombre no funciona con la Oclusión o el Thickness de ambiente?](../common-questions/why-matching-name-not-wor/why-is-matching-by-name-not-working-with-ambient-occlusion-thickness.md)
* [¿Por qué mi malla es completamente negra después de hornear?](../common-questions/why-mesh-fully-black-aft/why-is-my-mesh-fully-black-after-baking.md)

</td>
<td style="border: 0;" valign="top">

### Problemas comunes

* [Suavizado en costuras UV](../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md)
* [La salida de Baker es totalmente negra o está vacía](https://helpx.adobe.com/substance-3d/unlisted/documentation/bake/baker-output-is-fully-black-159451835.html)
* [Error de procesamiento con asignación de color desde malla](../common-issues/baking-failed-with-color/baking-failed-with-color-map-from-mesh.md)
* [Las cruces de sombreado negro son visibles en la superficie de la malla](../common-issues/black-shading-cross-are/black-shading-cross-are-visible-on-the-mesh-surface.md)
* [Las partes de la malla se sangran entre sí](../common-issues/mesh-parts-bleed-between/mesh-parts-bleed-between-each-other.md)
* [El mapa normal tiene degradados extraños y coloridos](../common-issues/normal-map-has-strange/normal-map-has-strange-colorful-gradients.md)
* [La textura normal parece faceteada](../common-issues/normal-texture-looks-fac/normal-texture-looks-faceted.md)
* [Las costuras son visibles después de hornear una textura normal](../common-issues/seams-are-visible-after/seams-are-visible-after-baking-a-normal-texture.md)
* [Costura visible en cada cara](../common-issues/seam-visible-every-face/seam-visible-on-every-face.md)

</td>
</tr>
</table>
