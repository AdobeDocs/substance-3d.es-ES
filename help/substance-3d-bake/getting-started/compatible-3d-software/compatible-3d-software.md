---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/getting-started/compatible-3d-software.html"
breadcrumb-title: ''
description: Descubre qué software 3D es compatible con Substance Bakers y aprende a preparar mallas para obtener resultados óptimos en la cocción.
helpx_creative_field: ""
helpx_description: bakers > Getting Started > Compatible 3D software
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Software 3D compatible
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 2%

---


# Software 3D compatible

La mayoría del software 3D es compatible con Substance Bakers siempre que exporten la geometría de malla como polígonos en formatos de archivo compatibles con las aplicaciones.

Sin embargo, no todo el software está a la par en términos de características y calidad al exportar estas mallas. Es por eso que es importante limpiar una malla correctamente y asegurarse de que sea compatible con los panaderos. Para obtener más información sobre cómo preparar una malla, consulta las distintas [Guías](../../guides/performances-and-opt/performances-and-optimizations.md).

## Compatibilidad de software

A continuación se muestra una lista de software 3D comúnmente conocido y su compatibilidad con los panaderos:

| *Nombre* | *Estado* |
| --- | --- |
| **Mezclador** | Compatible: requiere acoplar modificadores antes de exportar. |
| **Maya** | Compatible: requiere congelar el historial de transformación y eliminación antes de la exportación. |
| **3DS Max** | Compatible: requiere restablecer xForm antes de la exportación. |
| **MODO** | Compatible: Se recomienda utilizar el exportador de fichas de juego establecido en &quot;Malla estática irreal&quot;. |
| **Cinema 4D** | Compatible: requiere acoplar modificadores antes de exportar. |
| **zBrush** | No compatible: las mallas de bajo contenido de poli deben procesarse y limpiarse primero en otra aplicación 3D. Compatible: mallas de alto contenido de polietileno para hornear. |

## Formato del archivo

Al realizar el procesamiento de la geometría, es importante tener en cuenta también el formato de fichero utilizado. El formato de archivo definirá la cantidad de información que se guardará en la malla.

Tener demasiada información a veces puede ser perjudicial y dar lugar a errores. Por lo general, recomendamos probar diferentes formatos de archivo cuando se producen errores, ya que puede ser una forma fácil de solucionar problemas y determinar si el culpable está en el propio panadero o viene del software 3D.

A continuación se muestra un breve resumen de los dos formatos de archivo más comunes admitidos por los panaderos:

| Formato del archivo | Información |
| --- | --- |
| **FBX** | Autodesk FBX (Filmbox) es el formato de archivo principal utilizado por Autodesk Software, se puede escribir como texto o binario.  Es compatible con :<ul data-preserve-html="true"><li data-preserve-html="true">UV (conjuntos múltiples)</li><li data-preserve-html="true">Vértice, Tangente y Binormales</li><li data-preserve-html="true">Colores de vértice</li><li data-preserve-html="true">Cara triangular, cara cuádruple y cara N-Gon</li><li data-preserve-html="true">Cámaras</li><li data-preserve-html="true">Luces</li><li data-preserve-html="true">Subdivisiones de malla</li><li data-preserve-html="true">Grupos de suavizado</li><li data-preserve-html="true">Información sobre el material (como el color)</li><li data-preserve-html="true">Mapa de bits</li></ul> |
| **OBJ** | Wavefront OBJ es un formato de archivo basado en texto muy sencillo que admite :<ul data-preserve-html="true"><li data-preserve-html="true">UV (solo un conjunto)</li><li data-preserve-html="true">Vertex Normals</li><li data-preserve-html="true">Colores de vértice (solo si se exporta desde PincelPíxico)</li><li data-preserve-html="true">Cara triangular, cara cuádruple y cara N-Gon</li><li data-preserve-html="true">Color del material (si el archivo <strong>mtl</strong> está presente)</li></ul> |
