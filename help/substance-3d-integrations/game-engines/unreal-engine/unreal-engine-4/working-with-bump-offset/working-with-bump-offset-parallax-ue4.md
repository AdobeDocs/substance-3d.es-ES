---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/working-with-bump-offset-parallax-ue4.html"
breadcrumb-title: ''
description: Usa la asignación de desplazamiento de relieve con materiales Substance en Unreal Engine 4 para crear ilusión de profundidad y detalles de superficie.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Working with Bump Offset (Parallax) - UE4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Uso del desplazamiento de relieve (paralaje) - UE4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---


# Uso del desplazamiento de relieve (paralaje) - UE4

La asignación de **Desplazamiento de relieve** da a una superficie la ilusión de profundidad al modificar las coordenadas UV de forma creativa para ayudar a desplazar aún más los texeles de la superficie del objeto, lo que da la ilusión de que la superficie tiene más detalles de los que realmente tiene. En este ejemplo de Cómo, cubriremos no solo cómo puedes encontrar la expresión de material de desplazamiento de relieve, sino también cómo puedes utilizar el nodo de desplazamiento de saliente en tus materiales.

<https://docs.unrealengine.com/latest/INT/Engine/Rendering/Materials/HowTo/BumpOffset/>

Para utilizar la salida de height, debe hacer doble clic en la salida en la instancia de fábrica del Substance para crear el height. El height no está activado de forma predeterminada. A continuación, puede arrastrar esta salida de height al material.

![](../../../../assets/height-1.png){width="600px"}

Cree un nodo de desplazamiento de relieve y, a continuación, conecte el canal rojo del height al Height. A continuación, puede introducir un TextCoord en la entrada Coordenadas del desplazamiento de relieve. Por último, la salida del desplazamiento de relieve se conecta a la entrada UV para todas las texturas del Substance.

![](../../../../assets/bump.png){width="800px"}
