---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/getting-started/what-is-baking.html"
breadcrumb-title: ''
description: Descubre qué es el baking y aprende a guardar información de malla 3D en archivos de textura para mejorar tus materiales de Substance.
helpx_creative_field: ""
helpx_description: "bakers > Getting Started > What is Baking "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: '¿Qué es el horno? '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---


# ¿Qué es el Baking?

![](https://upload.wikimedia.org/wikipedia/commons/3/36/Normal_map_example.png)

&#x200B;>> 

(Créditos: [Paolo Cignoni](https://commons.wikimedia.org/wiki/File:Normal_map_example.png) - [CC BY-SA 1.0](https://creativecommons.org/licenses/by-sa/1.0)

El proceso de horneado se denomina **guardar información** relacionada con una **malla 3D** en un archivo de **textura** ([mapa de bits](https://en.wikipedia.org/wiki/Raster_graphics)). La mayoría de las veces, este proceso implica otra malla. En este caso, la información de la primera malla se transfiere a los UV de la segunda malla y, a continuación, se guarda en una textura.

Mientras que algunas aplicaciones pueden admitir el horneado de información en las propiedades de la malla (como los colores de los vértices), Substance Bakers solo permiten hornear la información hasta una textura. Sin embargo, pueden leer propiedades de malla y reducirlas a texturas (como colores de vértices).

## ¿Es necesario hornear?

El software Substance genera texturas que pueden mejorarse utilizando información relacionada con la geometría de malla.\
Muchos filtros y materiales pueden adaptarse a la geometría específica de una malla 3D observando las texturas horneadas. El horneado puede proporcionar información sobre dónde pueden estar las sombras ambientales, dónde están las aristas de la geometría y mucho más.

Por ejemplo: un coche viejo puede tener óxido aplicado en su parte inferior porque no se movió durante un tiempo. Hornear el mapa de posición permitirá saber dónde está la parte inferior en la malla que alimentará el generador de óxido y producirá la textura adaptada.

![](../../assets/examples.jpg){width="500px"}

## ¿Cómo funciona la cocción?

Cada panadero realiza acciones específicas para generar su propio resultado, pero en general el proceso de panadería implica dos métodos posibles:

* **Rebanando en una malla**: se basa en la malla actual para generar información.
* **Horneando de una malla a otra**: calcular la información desde una malla de origen y transferir el resultado a otra.

Este proceso de cocción se basa en las propiedades de la malla, por lo que la malla debe estar limpia y exenta de cualquier posible fallo en su geometría.

## ¿Qué tipo de información puedes hornear?

Muchos tipos de información pueden ser corroborados. Sin embargo, en general, solo se necesita un conjunto específico porque se pueden extrapolar para crear resultados más avanzados más adelante. Es por esto que hay un tipo común de proceso de panadería que se puede encontrar en múltiples software.

Como ejemplo, el software Substance puede generar el siguiente tipo de información:

* **oclusión ambiental** (sombras ambientales)
* Información de **Normal** (variaciones de detalles de superficie almacenadas como direcciones vectoriales)
* **Dirección** (hacia arriba o hacia abajo, izquierda o derecha, etc.)
* **Curvatura** (aristas y cavidades de la geometría)
* **Posición** (posición relativa de la geometría dentro de un cubo normalizado)

Consulte la [documentación de cada panadero](../../bakers-settings/bakers-settings.md) para obtener más información.

## Diferencia entre panaderos &#39;regulares&#39; y &#39;de malla&#39;

Dependiendo del proceso, los panaderos utilizan varias implementaciones. En términos generales, los panaderos **de mesh** se basan en técnicas de trazado de rayos para extraer y proyectar datos de un modelo a otro.
