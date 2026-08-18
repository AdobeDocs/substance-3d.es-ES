---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/curvature-from-mesh.html"
breadcrumb-title: ''
description: Genera texturas de curvatura precisas a partir de mallas de alto contenido de poli utilizando trazo de rayo para una detección precisa de los bordes.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Curvature from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Curvatura desde malla
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---


# Curvatura desde malla

La curvatura de malla baker genera una textura de curvatura a partir de mallas de alto contenido de poli. Es más lento que el panadero de base [curvatura](../../bakers-settings/curvature/curvature.md), pero produce resultados más precisos.

**Disponible en:**

* Substance Designer
* Substance Automation Toolkit
* Substance Painter

## Parámetros

| *Parámetro* | *Descripción* |
| --- | --- |
| **Rayos secundarios** | Cantidad de rayos emitidos para leer la geometría cercana. Un valor alto producirá menos ruido pero tardará más en calcularse. El valor predeterminado es 32. |
| **Radio de muestreo** | Hasta dónde se tiene en cuenta la geometría próxima para calcular la curvatura en la superficie de la geometría. Los valores altos pueden producir bordes más fuertes, mientras que los valores más bajos pueden producir bordes más finos, pero se pierde información. |
| **Relativo Al Cuadro Delimitador** | Define si el radio de muestreo es relativo al tamaño de la malla o si se define como una distancia basada en unidades. |
| **Intersección entre sí** | Coincidencia por nombre de los rayos de curvatura. Indica cómo deben coincidir los panaderos con la geometría de poly alta y baja. Se puede utilizar para filtrar el proceso de cocción sin necesidad de separar (explotar) las mallas manualmente.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Siempre</strong> (predeterminado): La malla de bajo contenido de polietileno se combina con todas las mallas de alto contenido de polietileno.</li><li data-preserve-html="true"><strong>Por nombre de malla</strong>: Filtre las mallas por su nombre para evitar que coincidan con geometría no deseada.</li></ul>Para obtener más información sobre la geometría coincidente, consulte: [Coincidencia por nombre](../../features/matching-by-name/matching-by-name.md). |
| **Límites automáticos de asignación de tonos** | Controla cómo deben escribirse los valores de curvatura en la textura. Si se activa, el rango de valor se normalizará entre 0 y 1 en función del valor mínimo y máximo encontrado durante el proceso de procesamiento. Si está desactivado, los valores mínimo y máximo se definen manualmente.  **Nota:** Al hornear mosaicos UDIM/UV, este parámetro debe deshabilitarse para que la asignación de tonos sea uniforme y no específica para cada mosaico; de lo contrario, esto podría crear uniones entre cada textura. Para encontrar los valores mínimos y máximos correctos manualmente, hornee primero con esta configuración habilitada y, a continuación, examine la consola/registro para ver qué valores generó el panadero. |
| **Mínimo de asignación de tonos** | Si **Límites automáticos de asignación de tonos** está deshabilitado, define el valor mínimo para escalar el resultado de curvatura para que se ajuste a la textura. |
| **Máximo de asignación de tonos** | Si **Límites automáticos de asignación de tonos** está deshabilitado, define el valor máximo para escalar el resultado de curvatura para que se ajuste a la textura. |
| **Mapa normal** | Ruta opcional a una textura normal. Se puede utilizar para reemplazar el cálculo interno del panadero. |
| **Espacio mundial** | Si se activa, la textura normal se interpreta como normal del espacio mundial en lugar de como espacio tangente. |
| **Orientación normal** | Formato de la textura Normal si está en Espacio Tangente. Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>DirectX</strong> (predeterminado)</li><li data-preserve-html="true"><strong>OpenGL</strong></li></ul> |
