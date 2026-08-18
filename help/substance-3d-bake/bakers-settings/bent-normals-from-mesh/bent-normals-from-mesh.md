---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/bent-normals-from-mesh.html"
breadcrumb-title: ''
description: Calcula texturas normales dobladas que describen la dirección media de la iluminación ambiental a partir de mallas de alta densidad de poli.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Bent Normals from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normales dobladas de la malla
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 3%

---


# Normales dobladas de la malla

Las normales de flexión del generador de mallas calculan una textura que describe la dirección media de la iluminación ambiental. Este panadero se deriva del panadero [Ambient Oclusión from Mesh](../../bakers-settings/ambient-occlusion-from/ambient-occlusion-from-mesh.md).

**Disponible en:**

* Painter
* Designer
* Automation Toolkit

## Parámetros

| *Parámetro* | *Descripción* |
| --- | --- |
| **Rayos secundarios** | Cantidad de rayos de oclusión. Un valor alto producirá menos ruido pero será más largo de calcular. |
| **Distancia Mínima Del Obturador** | Distancia mínima en la que los rayos de oclusión alcanzarán la alta geometría de poli**.** |
| **Distancia máxima del dispositivo de cierre** | Distancia máxima en la que los rayos de oclusión alcanzarán la alta geometría de poli. |
| **Relativo al cuadro delimitador** | Si se habilita, los cálculos de distancia de rayos se basan en el espacio normalizado (0 a 1) de la malla de baja densidad. Si está desactivada, el cálculo de la distancia de rayo se basa en las unidades especificadas en la malla de baja densidad cuando se exportó (metros, centímetros, etc.). |
| **Ángulo de pliego** | Ángulo de extensión máximo de los rayos de oclusión. El valor predeterminado es 180. |
| **Distribución** | Distribución angular de los rayos de oclusión.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Coseno</strong> (predeterminado)</li><li data-preserve-html="true"><strong>Uniforme</strong></li></ul> |
| **Omitir cara posterior** | Si se activa, los rayos de oclusión ignoran los golpes en una cara posterior (si la alta y normal polivinílica se enfrenta en la dirección opuesta a la baja y desde donde se dispara el rayo). La mayoría de las veces, esta configuración debe estar habilitada para evitar artefactos. |
| **Oclusión automática** | Coincidencia por nombre para rayos de oclusión. Indica cómo deben coincidir los panaderos con la geometría de poly alta y baja. Se puede utilizar para filtrar el proceso de cocción sin necesidad de separar (explotar) las mallas manualmente.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Siempre</strong> (predeterminado): La malla de bajo contenido de polietileno se combina con todas las mallas de alto contenido de polietileno.</li><li data-preserve-html="true"><strong>Por nombre de malla</strong>: Filtre las mallas por su nombre para evitar que coincidan con geometría no deseada.</li></ul>Para obtener más información sobre la geometría coincidente, consulte: [Coincidencia por nombre](../../features/matching-by-name/matching-by-name.md). |
| **Tipo de mapa** | Define el tipo de la textura de salida.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Espacio mundial</strong></li><li data-preserve-html="true"><strong>Espacio tangente</strong> (predeterminado)</li></ul> |
| **Orientación normal** | Controla el formato normal de la textura de salida si **Mat Type** está establecido en Espacio tangente. Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>OpenGL</strong> <strong> <br/></strong></li><li data-preserve-html="true"><strong>DirectX</strong> (predeterminado)<strong> <br/></strong></li></ul> |
