---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/working-with-displacement-ue4.html"
breadcrumb-title: ''
description: Activa la teselación y usa mapas de desplazamiento de materiales de Substance en Unreal Engine 4 para los detalles de la superficie.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Working with Displacement - UE4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'Uso de Desplazamiento: UE4'
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---


# Uso de Desplazamiento: UE4

Para trabajar con desplazamiento, deberá habilitar la teselación en el material.

![](../../../../assets/tess.png){width="600px"}

Para utilizar la salida de height, debe hacer doble clic en la salida en la instancia de fábrica del Substance para crear el height. El height no está activado de forma predeterminada. A continuación, puede arrastrar esta salida de height al material.

![](../../../../assets/height-1.png){width="800px"}

Una vez que haya agregado la salida de height al material, deberá crear algunos nodos para controlar el Desplazamiento Mundial y el Modificador de teselación.

1. Cree 2 parámetros escalares. Uno será Distancia y el otro será el multiplicador para teselación.
1. Multiplique el canal rojo desde el Height al parámetro Distancia
1. Agregue un nodo VertexNormalWS y múltiplelo con el resultado de la multiplicación en el paso 2.
1. Introduzca la multiplicación del Vértice Normal al Desplazamiento Mundial en el Material.
1. Tome el parámetro del multiplicador de teselación e introdúzcalo en el multiplicador de teselación del material.

![](../../../../assets/setup-3.png){width="800px"}

>[!NOTE]
>
> Las otras salidas de textura se han omitido en esta imagen para simplificar el gráfico. Aquí sólo se muestran los nodos Desplazamiento y Multiplicador para mayor claridad.
