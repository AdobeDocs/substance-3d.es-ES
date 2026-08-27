---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/guides/error-and-warning-messages.html"
breadcrumb-title: ''
description: Guía de referencia para todos los mensajes de error y advertencia que pueden aparecer al hacer un bake con el software de Substance.
helpx_creative_field: ""
helpx_description: bakers > Guides > Error and Warning Messages
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mensajes de error y de advertencia
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---


# Mensajes de error y de advertencia

A continuación se muestra la lista de todos los mensajes de error que pueden aparecer al hacer un bake con el software de Substance.

## Cualquier Baker

| *Mensaje* | *Descripción* |
| --- | --- |
| Baker no disponible. | Este mensaje de error suele ir seguido de mensajes de error adicionales, a menudo relacionados con problemas de GPU. Puede suceder si la GPU es demasiado antigua y no cumple los [requisitos técnicos](https://www.allegorithmic.com/products/tech-specs) del software. |
| El conjunto UV [X] no existe. | El Baker trató de trabajar con un conjunto de UV determinado que no está presente en la malla de bajo contenido de poli. |
| No se puede cargar la escena desde la URL. | Este mensaje significa que el baker no pudo cargar el archivo de malla, normalmente la malla de poli alta. La fuente de este mensaje puede ser una serie de razones:<ul data-preserve-html="true"><li data-preserve-html="true">El archivo de malla referenciado ya no existe.</li><li data-preserve-html="true">El archivo de malla está dañado y no se puede leer.</li><li data-preserve-html="true">Otra aplicación está editando la malla y no se puede leer.</li></ul> |

## Baker UV a SVG

| *Mensaje* | *Descripción* |
| --- | --- |
| No se han encontrado UV para la malla [nombre de la malla]. | No se encontraron UVs con respecto a una malla específica. Esto puede ocurrir si se importan varias mallas pero solo algunas de ellas tienen UV. |
| La escena no tiene UV. Cancelando hacer un bake. | Si ninguna malla de la escena tiene UV, el proceso de hace un bake se cancela. |

## Baker de posición

| *Mensaje* | *Descripción* |
| --- | --- |
| Malla [nombre de malla] no tiene posiciones. | La malla de poli baja no tiene posiciones de vértice. |
| La malla [nombre de la malla] no tiene UV para el conjunto UV [X]. | El Baker trató de trabajar con un conjunto de UV determinado que no está presente en la malla de bajo contenido de poli. |

## Cualquier Baker &quot;Desde malla&quot;

| *Mensaje* | *Descripción* |
| --- | --- |
| No se encontraron normales de vértice en la malla [nombre de malla]. | No se encontraron normales de vértice en la malla dada. Normalmente, nunca sucede porque las normales de vértice se vuelven a calcular si la malla no las tiene. Puede que se deba a un plugin de espacio tangente personalizado defectuoso. |
| No se han encontrado tangentes de vértices en la malla [nombre de malla]. | Igual que el anterior. |
| No se han encontrado binormales de vértice en la malla [nombre de malla]. | Igual que el anterior. |
| No se encontraron colores de vértice en la malla [nombre de malla]. | No se encontraron colores de vértice en la malla especificada. Esto puede suceder si al menos una malla secundaria de la malla de alta densidad no tiene ningún color de vértice definido. |
| No hay suficientes datos en la capa superior para usar el baker seleccionado. Abortando Bake. | Precedido de al menos uno de los mensajes anteriores. Normalmente, si solo falta un bit de datos en la escena (ejemplo : solo una malla en la escena poli alta no tiene colores de vértice), el proceso de horneado llenar los datos que faltan con ceros, y seguir horneando. Si faltan demasiados datos, este mensaje se envía y el proceso de procesamiento se detiene. |

## Textura transferida desde malla

| *Mensaje* | *Descripción* |
| --- | --- |
| Error al cargar la textura detallada. | No se pudo cargar la textura definida en la configuración del panadero. Podría deberse a que el archivo falta realmente en el disco o a que está dañado y no es legible. |
