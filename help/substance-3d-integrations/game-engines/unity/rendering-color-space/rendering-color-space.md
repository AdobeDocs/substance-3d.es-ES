---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/game-engines/unity/rendering-color-space.html"
breadcrumb-title: ''
description: Configure los ajustes del espacio de color de Unity para garantizar la representación correcta de los materiales Substance con sombreadores basados en la física.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Rendering Color Space
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Renderizado del espacio de color
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---


# Renderizado del espacio de color

Las texturas Substance están diseñadas para usarse con un sombreador basado en la física. Para obtener los mejores resultados, debe establecer el espacio de color en lineal en Configuración del reproductor de Unity.

1. Vaya a Editar>Ajustes del proyecto>Reproductor
1. En la sección Procesamiento, cambie el Espacio de color a Lineal. (De forma predeterminada, Unity usa el espacio Gamma, que es incorrecto y dará como resultado que el color de la textura tenga un aspecto incorrecto).

   >[!NOTE]
   >
   > **Información**
   > 
   > Las opciones de sRGB en texturas se desactivan si la configuración de Espacio de color en Unity está establecida en Gamma

   ![](../../../assets/rendering-4.png){width="600px"}
