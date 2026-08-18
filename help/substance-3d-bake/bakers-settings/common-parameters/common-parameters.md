---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/common-parameters.html"
breadcrumb-title: ''
description: Obtenga más información sobre los parámetros comunes que se aplican a todos los panaderos y cómo configurarlos para una generación óptima de texturas.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Common Parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Parámetros comunes
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 1%

---


# Parámetros comunes

Los parámetros comunes se aplican a todos los panaderos. Estos parámetros generalmente definen cómo se comportarán los panaderos y trabajarán con mallas de alto contenido de polietileno, pero cómo se generarán las texturas finales. Algunos de estos parámetros pueden ser reemplazados por panaderos específicos.

Aunque la mayoría de estos parámetros están disponibles en todo el software (incluido el kit de herramientas de automatización de Substance), su comportamiento puede variar ligeramente; o puede que algunos no estén disponibles en función del flujo de trabajo y la implementación del software.

## Parámetros generales

Estos parámetros afectan a la forma en que los panaderos generan texturas.

| *Nombre* | *Descripción* |
| --- | --- |
| **Tamaño**(Tamaño predeterminado o Tamaño de salida) | Controlar la resolución de textura de salida de pandeo (en píxeles).Valores disponibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>32</strong></li><li data-preserve-html="true"><strong>64</strong></li><li data-preserve-html="true"><strong>128</strong></li><li data-preserve-html="true"><strong>256</strong></li><li data-preserve-html="true"><strong>512</strong></li><li data-preserve-html="true"><strong>1024</strong></li><li data-preserve-html="true"><strong>2048</strong> (predeterminado)</li><li data-preserve-html="true"><strong>4096</strong></li><li data-preserve-html="true"><strong>8192</strong></li></ul>También se admiten resoluciones que no sean cuadradas, por ejemplo: 2048x1024 (relación 2:1). En Substance Designer, este parámetro puede ser reemplazado por el propio panadero. |
| **Formato** | Formato de archivo de las texturas horneadas.*No disponible en Substance Painter.* Consulte: [Cómo exportar los mapas con bake](../../common-questions/how-export-the-baked-maps/how-to-export-the-baked-maps.md). |
| **Suavizado** | Controla el suavizado, que puede mejorar la calidad de las texturas al horno y reducir el suavizado en los lugares donde se conectan las diferentes geometrías.Para obtener más información sobre el suavizado, consulte: [Suavizado en uniones UV](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md) y [Suavizado en Wikipedia](https://en.wikipedia.org/wiki/Aliasing).Valores disponibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Ninguno</strong> (predeterminado)</li><li data-preserve-html="true"><strong>Submuestreo 2x2</strong></li><li data-preserve-html="true"><strong>Submuestreo 4x4</strong></li><li data-preserve-html="true"><strong>Submuestreo 8x8</strong></li></ul>  **Nota:** La activación del suavizado puede aumentar significativamente el tiempo de procesamiento, ya que el suavizado funciona calculando la textura a una resolución más alta y, a continuación, volviendo a escalarla al tamaño seleccionado originalmente. Esto significa que una textura 2K con un submuestreo 2x2 calculará realmente una textura 4K.A veces es preferible aumentar el número de rayos en el panadero en lugar de aumentar el submuestreo. Podría lograr mejores resultados sin esperar demasiado tiempo. |
| **Conjunto UV** | Controla qué UV de la malla de baja densidad se utilizarán para calcular las texturas horneadas.*No disponible en Substance Painter.* |
|  |  |
| **Dilatación (px)** | Dilate o amplíe los píxeles de las coordenadas UV exteriores o su borde en función de la cantidad de píxeles dados. Esta operación permite evitar costuras en los bordes UV cuando estos bordes no están perfectamente alineados con los píxeles de textura o cuando se reduce la resolución de textura (por ejemplo: mipmaps). Este es un proceso posterior aplicado después del proceso de cocción. A veces también se le puede llamar &quot;relleno&quot;.Para obtener más información sobre la dilatación, consulte: [Suavizado en uniones UV](../../common-issues/aliasing-on-uv-seams/aliasing-on-uv-seams.md) y [Relleno](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/padding-134643719.html). |
| **Aplicar difusión** | Si se activa, el exterior de las coordenadas UV se rellenará con colores de degradado suavizados basados en los bordes UV. Este proceso garantiza que cuando se reduce el tamaño de la textura se mantenga estable y no se creen costuras demasiado visibles (por ejemplo: mipmaps). Este es un proceso posterior aplicado después del proceso de cocción. |
| **Normales promedio** | Si está activada, calcula la normal media de un vértice para saber en qué dirección enviar rayos durante el proceso de coincidencia de malla del baking. Si se desactiva, los rayos seguirán los vértices normales originales de la malla. |

## Parámetros High-Poly

Los siguientes parámetros controlan el horneado de malla de alto a bajo contenido de poli (panaderos &quot;de malla&quot;).

| *Nombre* | *Descripción* |
| --- | --- |
| **Mallas de alta definición** | Una lista de archivos (o recursos de paquetes de Substance) que contiene mallas de alto nivel. Los panaderos los cargan en la memoria cuando el proceso de panadería comienza a calcular información diferente y a guardar esa información de malla en texturas. Esta lista se omite si está habilitado &quot;**Usar baja como alta definición**&quot;. |
| **Usar baja como alta definición** o **Usar malla de baja densidad como malla de alta densidad** | Si se habilita, la lista de mallas de alto contenido polivinílico proporcionada a los panaderos se ignorará y la malla de bajo contenido polivinílico se horneará sobre sí misma.Este parámetro es útil cuando se trabaja directamente con una malla de alta densidad. Por ejemplo, al hornear una textura de oclusión ambiental para un coche de alta polietileno con este ajuste activado, la distancia de rayos se ignora y el panadero producirá una cocción perfecta (no hay pérdida de rayos ni discrepancia de geometría). |
|  |  |
| **Establecer distancia con jaula** o **Usar jaula** | Indica si se debe utilizar un archivo de malla de jaula en el proceso de cocción en lugar de utilizar valores de distancia de rayo. La jaula controla la distancia máxima del rayo y la dirección. |
| **Archivo de jaula** | Ruta al archivo de malla que contiene la jaula. |
| **Valor frontal** o **Distancia frontal máxima** | Controla la distancia por encima de la superficie de baja polimerización en la que el rayo debe empezar a encontrar cualquier geometría de alta polimerización a lo largo de su trazado.*Esta configuración no tiene efecto cuando se usa una jaula.* |
| **Valor posterior** o **Distancia posterior máxima** | Controla la distancia que hay por debajo de la superficie de baja polimerización en la que el rayo debe detenerse para encontrar cualquier geometría de alta polimerización a lo largo de su trazado.*Esta configuración no tiene efecto cuando se usa una jaula.* |
| **Relativo al cuadro delimitador** | Si se activa, la distancia de rayos y otros cálculos basados en el tamaño se basan en el espacio normalizado de la malla de baja densidad. Si está desactivado, el cálculo de la distancia de rayo se basa en las unidades especificadas en la malla de baja densidad cuando se exportó (metros, centímetros, etc.). En ocasiones, puede resultar útil desactivar este ajuste e introducir la distancia de rayo manualmente cuando un objeto tiene medidas precisas. |
|  |  |
| **Coincidencia** | Indica cómo deben coincidir los panaderos con la geometría de poly alta y baja. Se puede utilizar para filtrar el proceso de cocción sin necesidad de separar (explotar) las mallas manualmente.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Siempre</strong> (predeterminado): La malla de bajo contenido de polietileno se combina con todas las mallas de alto contenido de polietileno.</li><li data-preserve-html="true"><strong>Por nombre de malla</strong>: Filtre las mallas por su nombre para evitar que coincidan con geometría no deseada.</li></ul>Para obtener más información sobre la geometría coincidente, consulte: [Coincidencia por nombre](../../features/matching-by-name/matching-by-name.md). |
| **Sufijos de coincidencia** o **Sufijo de malla de alta densidad** **Sufijo de malla de baja densidad** | Sufijos de nombre de malla para identificar y agrupar la geometría al utilizar la función Coincidencia por nombre. Sufijos disponibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Malla de poli baja</strong>: sufijo para identificar mallas de poli bajas en la escena</li><li data-preserve-html="true"><strong>Malla de alta densidad</strong>: sufijo para identificar mallas de poli altas en la escena</li><li data-preserve-html="true"><strong>Ignorar caras posteriores</strong>: sufijo para identificar mallas que deben omitir determinados panaderos (como la [Oclusión ambiental desde malla](../../bakers-settings/ambient-occlusion-from/ambient-occlusion-from-mesh.md))</li></ul>Para obtener más información sobre la geometría coincidente, consulte: [Coincidencia por nombre](../../features/matching-by-name/matching-by-name.md) . |
|  |  |
| **Usar corrección de sesgo** | Si se habilita, la dirección del rayo se calculará a partir de **Normal promedio** o de la geometría normal original, dependiendo de la textura de entrada. Los valores negros de la textura utilizan la media normal calculada, mientras que los valores blancos utilizan la malla original normal.*No disponible en Substance Painter.* |
| **Mapa de sesgo** | Ruta al archivo de textura utilizado para sesgar la proyección de rayos. |
| **Invertir corrección de sesgo** | Invierte la lectura de la textura de entrada (el negro se vuelve blanco y el blanco se vuelve negro). |
