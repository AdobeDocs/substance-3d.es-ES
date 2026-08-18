---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/position-map-from-mesh.html"
breadcrumb-title: ''
description: Calcule mapas de posición precisos a partir de mallas de alta densidad para capturar información precisa de la ubicación de la geometría.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Position map from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mapa de posición desde malla
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---


# Mapa de posición desde malla

El mapa de posición del panel de malla calcula la ubicación de la geometría de malla de alta densidad y la guarda en una textura. Es similar al panadero de posición base, pero puede producir resultados más precisos.

**Disponible en:**

* Substance Designer
* Substance Automation Toolkit

## Parámetros

| *Parámetro* | *Descripción* |
| --- | --- |
| **Modo** | Controla la información que se calculará en la textura de posición.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Todos los ejes:</strong> Hornea la posición de los ejes X, Y y Z en los canales de RGB de la textura de salida.</li><li data-preserve-html="true"><strong>Un eje:</strong> Convierte un solo eje en la textura de salida como una imagen en escala de grises.</li></ul> |
| **Eje** | Define qué eje se debe calcular si el parámetro **Mode** está establecido en **One axis**. |
| **Tipo de normalización** | Define cómo escalar los valores de posición por eje.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Box:</strong> normaliza cada eje según el volumen de la malla (longitud del cuadro delimitador).</li><li data-preserve-html="true"><strong>BSphere:</strong> normaliza todos los ejes según el radio del volumen de la malla (esfera delimitadora).</li></ul> |
| **Escala de normalización** | Define cómo escalar los valores de posición en función de la malla.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Por Material</strong>: se escalan de modo que estén entre 0 y 1 para cada material (conjunto de texturas).</li><li data-preserve-html="true"><strong>Escena completa</strong> (predeterminado): se escalan para tener en cuenta toda la malla. Esto permite valores de posición continuos entre objetos y materiales (conjuntos de texturas).</li></ul> |
