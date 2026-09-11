---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/tiling-substance-ue4.html"
breadcrumb-title: ''
description: Coloca en mosaico texturas Substance en Unreal Engine 4 añadiendo nodos de coordenadas de textura y parámetros escalares a los materiales.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Tiling Substance - UE4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance de baldosas - UE4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---


# Substance de baldosas - UE4

Para estructurar una textura de sustancia, deberá añadir un nodo de coordenadas de textura y multiplicarlo por el parámetro escalar.

<https://docs.unrealengine.com/latest/INT/Engine/Rendering/Materials/ExpressionReference/Coordinates/#texturecoordinate>

Para crear parámetros para el mosaico U y V, puede utilizar un vector Anexar y multiplicarlo por TextCoord. Esto le permite definir de forma independiente las cantidades de azulejo U y V.

![](../../../../assets/tiling-3.png){width="800px"}
