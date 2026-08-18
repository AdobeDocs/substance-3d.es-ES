---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/bakers-settings/curvature.html"
breadcrumb-title: ''
description: Extraiga la información de curvatura de la malla para crear texturas que realcen las cavidades y aristas de la geometría.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Curvature
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Curvatura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 2%

---


# Curvatura

El panadero de curvatura permite extraer una textura de curvatura. Esta textura contiene información de cavidades y aristas relacionada con la geometría.

Las propiedades de textura se definen como:

* Los valores negros representan áreas cóncavas.
* Los valores blancos representan áreas convexas.
* Los valores de gris representan áreas neutras (principalmente planas).

**Disponible en :**

* Substance Designer
* Substance Automation Toolkit
* Substance Painter

## Parámetros

| *Parámetro* | *Descripción* |
| --- | --- |
| **Algoritmo** | Define cómo se calculará la información de curvatura en la malla. |
| **Detalles** | Controla la intensidad de la información de la curvatura. Un valor alto puede producir más detalles pero menos sutil. |
| **Habilitar juntas** | Si se habilita, el panadero intentará reducir las costuras entre las Islas de UV copiando los texeles de los bordes de un lado al otro. |
| **Costuras** **Intensidad** | Si **Habilitar juntas** está habilitado, este parámetro controla el grado de solidez de la fijación de las juntas. |
