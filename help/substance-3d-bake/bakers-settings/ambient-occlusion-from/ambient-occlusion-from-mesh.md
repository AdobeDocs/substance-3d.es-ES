---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/bakers-settings/ambient-occlusion-from-mesh.html"
breadcrumb-title: ''
description: Hornea texturas de oclusión ambiental precisas de mallas de alto contenido de poli utilizando técnicas de trazado de rayos para mejorar el realismo.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Ambient Occlusion from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Oclusión ambiental desde malla
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 2%

---


# Oclusión ambiental desde malla

La Oclusión Ambient del panadero de malla permite hornear una textura de Oclusión Ambient a partir de mallas de poliéster altas. Es más lento que el panadero de base [oclusión ambiente](../../bakers-settings/ambient-occlusion/ambient-occlusion.md), pero produce resultados más precisos.

**Disponible en:**

* Substance Designer
* Substance Automation Toolkit
* Substance Painter

## Parámetros

| *Parámetro* | *Descripción* |
| --- | --- |
| **Rayos secundarios** | Cantidad de rayos de oclusión. Un valor alto producirá menos ruido pero tardará más en calcularse. El valor predeterminado es 64. |
| **Distancia Mínima Del Obturador** | Distancia mínima en la que los rayos de oclusión alcanzarán la alta geometría de poli. El valor predeterminado es 0,00001. |
| **Distancia máxima del dispositivo de cierre** | Distancia máxima en la que los rayos de oclusión alcanzarán la alta geometría de poli. El valor predeterminado es 0.1. |
| **Relativo al cuadro delimitador** | Si se activa, las unidades son relativas al cuadro delimitador del objeto (siendo 1,0 la longitud diagonal del cuadro delimitador). Si está desactivada, las unidades utilizadas para las distancias de oclusión mínima y máxima son las definidas al exportar la malla (metros, centímetros o las unidades que sean de la escena exportada). |
| **Ángulo de pliego** | Ángulo de extensión máximo de los rayos de oclusión. El valor predeterminado es 180. |
| **Distribución** | Distribución angular de los rayos de oclusión. Define cómo se dispersan los rayos dentro de un cono del tamaño del ángulo de propagación.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Coseno</strong> (predeterminado): Realista, pero puede dar lugar a una línea blanca en áreas ocluidas muy finas. Más adecuado para el sombreado y la iluminación.</li><li data-preserve-html="true"><strong>Uniforme</strong>: Resulta útil para crear degradados lineales. Más adecuado para el enmascaramiento de capas y otros filtros.</li></ul> |
| **Omitir cara posterior** | Estos parámetros definen si los rayos de oclusión ignoran los golpes en una cara posterior (si la cara normal de poly alta se enfrenta en la dirección opuesta a la de poly baja desde donde se dispara el rayo). La mayoría de las veces, esta configuración debe estar habilitada para evitar artefactos. Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Nevers</strong> (predeterminado): Las caras posteriores nunca se ignoran</li><li data-preserve-html="true"><strong>Siempre</strong>: Las caras posteriores siempre se omiten</li><li data-preserve-html="true"><strong>Por nombre de malla</strong>: Las caras posteriores solo se omiten para las mallas que coinciden con la palabra clave suffix. Consulte los [parámetros comunes](../../bakers-settings/common-parameters/common-parameters.md).</li></ul> |
| **Oclusión automática** | Coincidencia por nombre para rayos de oclusión. Indica cómo deben coincidir los panaderos con la geometría de poly alta y baja. Se puede utilizar para filtrar el proceso de cocción sin necesidad de separar (explotar) las mallas manualmente.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Siempre</strong> (predeterminado): La malla de bajo contenido de polietileno se combina con todas las mallas de alto contenido de polietileno.</li><li data-preserve-html="true"><strong>Por nombre de malla</strong>: Filtre las mallas por su nombre para evitar que coincidan con geometría no deseada.</li></ul>Para obtener más información sobre la geometría coincidente, consulte: [Coincidencia por nombre](../../features/matching-by-name/matching-by-name.md). |
| **Mapa normal** | Ruta opcional a una textura normal. Se puede utilizar para reemplazar el cálculo interno del panadero. |
| **Espacio mundial** | Si se activa, la textura normal se interpreta como normal del espacio mundial en lugar de como espacio tangente. |
| **Orientación normal** | Formato de la textura Normal si está en Espacio Tangente. Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>DirectX</strong> (predeterminado)</li><li data-preserve-html="true"><strong>OpenGL</strong></li></ul> |
| **Atenuación** | Define cómo se atenúa la oclusión mediante la distancia del oclusor.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Ninguno</strong>: sin atenuación.</li><li data-preserve-html="true"><strong>Lineal</strong> (predeterminado): atenuación progresiva.</li><li data-preserve-html="true"><strong>Suave</strong>: atenuación suave.</li></ul> |
| **Plano de tierra** | Si está activada, simule un plano bajo el cuadro delimitador de la malla en el eje XZ para colisionar con los rayos secundarios. Esto simula sombras procedentes de un plano de suelo invisible. |
| **Desplazamiento de plano de tierra** | Permite desplazar el plan fuera de la malla para reducir la intensidad del efecto. El valor es absoluto y no relativo al tamaño de malla. |
