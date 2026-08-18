---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/guides/triangulating-before-baking.html"
breadcrumb-title: ''
description: Conozca cómo la triangulación de malla afecta a los resultados de procesamiento y conozca las prácticas recomendadas para preparar la geometría.
helpx_creative_field: ""
helpx_description: bakers > Guides > Triangulating before baking
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Triangulando antes de hornear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# Triangulando antes de hornear

Las mallas 3D se pueden definir con polígonos con varios bordes por cara. Por lo general a través de cuádruples (4 bordes), a veces más (n-gons).\
Sin embargo, el software transforma esos polígonos en triángulos más adelante porque es más fácil gestionar y realizar cálculos con ellos (especialmente en la GPU).

## ¿Cómo puede afectar la triangulación a una malla?

![](../../assets/triangulation.jpg)

No hay **soluciones estándar** para convertir Quad/N-Gons en triángulos. Como se muestra en la imagen anterior, varias opciones son válidas.\
Es poco probable que los panaderos triangulen las mallas como lo haría un motor de juego porque elegimos un algoritmo específico sobre otro.

## ¿Por qué triangular antes de hornear?

El proceso de cocción leerá la geometría y, a continuación, codificará la información en texturas.\
Como esa información se basa en UV y, a veces, en la topología de malla, otro software podría descodificar la información incorrectamente si no leen la geometría de la misma manera que cuando aplican la textura.

En la imagen siguiente, puede ver la malla de baja densidad en la parte superior izquierda y la malla de alta densidad en la parte superior derecha.\
En la parte inferior se encuentra el low-poly con el mapa normal cocido del high-poly. La malla de la izquierda utiliza una triangulación idéntica a la utilizada por el Substance Painter al hornear. La malla de la derecha no funciona y muestra artefactos negros. Esto se debe a que hay una discrepancia entre la forma en que se horneó el mapa normal y la forma en que se triangula actualmente la malla. Esto se puede corregir **actualizando la malla y/o reorganizando**.

![](../../assets/example-triangulation-artifact.jpg)
