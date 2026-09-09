---
helpx_url: 'https://helpx.adobe.com/substance-3d-bake/getting-started/what-is-baking.html'
breadcrumb-title: ''
description: Descubre lo que es hacer un bake y aprende a guardar información de malla 3D en archivos de textura para mejorar los materiales de Substance.
helpx_creative_field: ''
helpx_description: 'bakers > Getting Started > What is Baking '
helpx_experience_level: ''
helpx_learn_topic: ''
helpx_tags: ''
title: 'Lo que está Haciendo un bake '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0a948aa65b787c0f84e0af681dbe74021e878687
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---


# ¿Qué está Haciendo un bake?

![](https://upload.wikimedia.org/wikipedia/commons/3/36/Normal_map_example.png)

(Créditos: [Paolo Cignoni](https://commons.wikimedia.org/wiki/File:Normal_map_example.png) - [CC BY-SA 1.0](https://creativecommons.org/licenses/by-sa/1.0))

Haciendo un bake es el nombre del proceso sobre **guardar información** relacionada con una **malla 3D** en un archivo de **textura** ([mapa de bits](https://en.wikipedia.org/wiki/Raster_graphics)). La mayoría de las veces, este proceso implica otra malla. En este caso, la información de la primera malla se transfiere a las UV de la segunda malla y, a continuación, se guarda en una textura.

Aunque algunas aplicaciones pueden admitir hacer un bake información en las propiedades de la malla (como los colores de los vértices), Substance Bakers solo permiten hacer un bake información en una textura. Sin embargo, pueden leer las propiedades de malla y hacer un bake a texturas (como los colores de los vértices).

## ¿Es necesario hacer un bake?

El software Substance genera texturas y estas texturas se pueden mejorar utilizando información relacionada con la geometría de malla.\
Muchos filtros y materiales pueden adaptarse a la geometría específica de una malla 3D observando las texturas hechas un bake. Hacer un bake puede proporcionar información sobre dónde pueden estar las sombras de ambiente, dónde están las aristas de la geometría y mucho más.

Por ejemplo: un coche viejo puede tener óxido aplicado en su parte inferior porque no se movió durante un tiempo. Hacer un bake el mapa de posición permitirá saber dónde se encuentra el fondo en la malla que alimentará al generador de óxido y producirá la textura adaptada.

![](../../assets/examples.jpg){width="500px"}

## ¿Cómo funciona hacer un bake?

Cada baker realiza acciones específicas para generar su propio resultado, pero en general el proceso de hacer un bake implica dos métodos posibles:

* **Haciendo un bake en una malla** : se basa en la malla actual para generar información.
* **Haciendo un bake de una malla a otra** : calcular la información desde una malla de origen y transferir el resultado a otra.

Este proceso de hace un bake se basa en las propiedades de la malla, por lo que la malla debe estar limpia y exenta de posibles fallos en su geometría.

## ¿Qué tipo de información puedes hacer un bake?

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
