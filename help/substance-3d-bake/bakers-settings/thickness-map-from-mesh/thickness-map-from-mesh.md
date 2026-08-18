---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/bakers-settings/thickness-map-from-mesh.html"
breadcrumb-title: ''
description: Genera mapas de thickness echando rayos hacia dentro desde las superficies de malla para usarlos en sombreadores de CSS y máscaras.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Thickness Map from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mapa de grosor de malla
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 5%

---


# Mapa de grosor de malla

El mapa de Thickness de la malla es muy similar al panadero de la oclusión ambiente, pero arroja rayos desde la superficie de la malla hacia el interior. Esta textura se puede utilizar en un sombreado de dispersión subsuperficial (SSS) o para enmascarar texturas.

Las propiedades de textura se definen como:

* Los valores negros representan las partes delgadas del modelo.
* Los valores blancos representan las partes gruesas del modelo.

**Disponible en:**

* Substance Painter
* Substance Designer
* Substance Automation Toolkit

## Parámetros

| *Parámetro* | *Descripción* |
| --- | --- |
| **Rayos secundarios** | Cantidad de rayos de oclusión. Un valor alto producirá menos ruido pero tardará más en calcularse. El valor predeterminado es 64. |
| **Distancia Mínima Del Obturador** | Distancia mínima en la que los rayos de oclusión alcanzarán la alta geometría de poli. El valor predeterminado es 0,00001. |
| **Distancia máxima del dispositivo de cierre** | Distancia máxima en la que los rayos de oclusión alcanzarán la alta geometría de poli. El valor predeterminado es 0.1. |
| **Relativo al cuadro delimitador** | Si se activa, las unidades son relativas al cuadro delimitador del objeto (siendo 1,0 la longitud diagonal del cuadro delimitador). Si está desactivada, las unidades utilizadas para las distancias de oclusión mínima y máxima son las definidas al exportar la malla (metros, centímetros o las unidades que sean de la escena exportada). |
| **Ángulo de pliego** | Ángulo de extensión máximo de los rayos de oclusión. El valor predeterminado es 180. |
| **Distribución** | Distribución angular de los rayos de oclusión.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Coseno</strong> (predeterminado)</li><li data-preserve-html="true"><strong>Uniforme</strong></li></ul> |
| **Omitir cara posterior** | Si se activa, los rayos de oclusión ignoran los golpes en una cara posterior (si la alta y normal polivinílica se enfrenta en la dirección opuesta a la baja y desde donde se dispara el rayo). La mayoría de las veces, esta configuración debe estar habilitada para evitar artefactos. |
| **Oclusión automática** | Coincidencia por nombre para rayos de oclusión. Indica cómo deben coincidir los panaderos con la geometría de poly alta y baja. Se puede utilizar para filtrar el proceso de cocción sin necesidad de separar (explotar) las mallas manualmente.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Siempre</strong> (predeterminado): La malla de bajo contenido de polietileno se combina con todas las mallas de alto contenido de polietileno.</li><li data-preserve-html="true"><strong>Por nombre de malla</strong>: Filtre las mallas por su nombre para evitar que coincidan con geometría no deseada.</li></ul>Para obtener más información sobre la geometría coincidente, consulte: [Coincidencia por nombre](../../features/matching-by-name/matching-by-name.md). |
| **Normalización automática** | Define si los valores de salida deben escalarse para que se ajusten a un intervalo de 0 a 1 (el punto más brillante se establece en blanco puro y el punto más oscuro se establece en negro puro). |
