---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/world-space-direction.html"
breadcrumb-title: ''
description: Calcula las direcciones de los vectores en el espacio de entorno y guárdalos en texturas para aplicar efectos direccionales y aplicar máscaras.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > World Space Direction
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dirección de espacio de mundo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 4%

---


# Dirección de espacio de mundo

El panadero World Space Direction permite calcular una dirección vectorial en el espacio del mundo en una textura.

**Disponible en :**

* Substance Designer
* Substance Automation Toolkit

## Parámetros

| *Parámetro* | *Descripción* |
| --- | --- |
| **Dirección de entrada** | Define a partir de qué entrada se calcula la dirección.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>De la textura</strong>: la dirección vectorial se define mediante una textura de entrada.</li><li data-preserve-html="true"><strong>De vector uniforme</strong> (predeterminado): la dirección del vector se define con los reguladores X, Y, Z.</li></ul> |
| **Orientación normal** | Define si el formato normal de la textura de salida. Esto invierte el canal verde dependiendo del formato.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>OpenGL</strong></li><li data-preserve-html="true"><strong>DirectX</strong> (predeterminado)</li></ul> |
| **X Y Z** | Reguladores para definir los 3 componentes del vector de dirección, si **Dirección de entrada** está establecido en **Desde vector uniforme**. |
| **Archivo de dirección** | Ruta al archivo de textura de entrada para definir el vector de dirección, si **Dirección de entrada** está establecido en **Desde textura**. |
