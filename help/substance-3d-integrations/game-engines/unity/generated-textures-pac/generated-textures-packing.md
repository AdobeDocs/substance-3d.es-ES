---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/game-engines/unity/generated-textures-packing.html"
breadcrumb-title: ''
description: Conozca cómo Substance genera texturas en Unity y configure el empaquetado de texturas para obtener entradas de sombreado óptimas.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Generated Textures (Packing)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Texturas generadas (Empaquetado)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 6%

---


# Texturas generadas (Empaquetado)

Las texturas generadas muestran las salidas del Substance calculadas por el Substance Engine para crear texturas. Estas texturas se introducen en las entradas del sombreado. De forma predeterminada, sólo se crean las entradas base utilizadas por el sombreado. Si la opción &quot;Generar todas las salidas&quot; está activada, todas las texturas se mostrarán aquí.

![](../../../assets/screen-shot-2022-03-29-at-1-24-16-pm-copy.png)

Cuando la opción Generar todas las salidas está activada

![](../../../assets/screen-shot-2022-03-29-at-1-29-35-pm-copy.png)

## Uso

1. Al seleccionar un icono de textura, se seleccionará la textura en la ventana del proyecto. Esto no funciona con materiales de tiempo de ejecución porque no se generan texturas en la carpeta del proyecto.
1. El botón sRGB funciona de forma similar a la opción sRGB (textura de color) de los Ajustes de importación de textura. Permite definir si una textura debe interpretarse en un espacio gamma (sRGB) o lineal. El complemento Substance gestiona esta interpretación automáticamente, pero puede anularse si es necesario.

   | Salida de Substance | sRGB |
   | --- | --- |
   | Color base | Activado |
   | Difusión | Activado |
   | Especular | Activado |
   | Normal | Desactivado |
   | Metálico | Desactivado |
   | Rugosidad | Desactivado |
   | Brillo | Desactivado |
   | Altura | Desactivado |
   | Oclusión ambiental | Desactivado |

## Canales de empaquetado

Puede empaquetar una textura en el canal alfa de otra textura mediante el menú desplegable. Cada textura generada tiene un menú desplegable que contiene una lista de todas las salidas de textura generadas por los materiales de Substance. Simplemente elija un mapa de la lista para empaquetarlo en el canal alfa de la textura. La opción Origen es el canal alfa de la textura.

En esta imagen, he seleccionado el mapa de height:

![](../../../assets/screen-shot-2022-03-29-at-2-48-33-pm.png)

En la siguiente imagen, puede ver que la salida de height se empaqueta en el canal alfa del mapa de color base.

![](https://helpx-prod.scene7.com/is/image/HelpxProd/screen-shot-2022-03-29-at-2-53-20-pm-copy?$png$&jpegSize=200&wid=1248)

## Asignación de textura de salida

Además, la textura de salida se puede asignar individualmente a las entradas de superficie de los materiales Unity mediante la sección Asignación de textura de salida . Las texturas de salida generadas por el archivo .sbsar se mostrarán en la columna izquierda y las entradas de superficie de unidad disponibles aparecerán en la columna derecha. Esta última se puede cambiar a través de los menús desplegables.

![](../../../assets/image2023-3-27-14-30-24.png)
