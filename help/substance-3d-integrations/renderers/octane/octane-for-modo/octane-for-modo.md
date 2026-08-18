---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/renderers/octane/octane-for-modo.html"
breadcrumb-title: ''
description: Utilice materiales Substance con el procesador Octane en MODO a través de materiales de Live DB y configuraciones de salida adecuadas.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Octane > Octane for MODO
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Octano para MODO
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# Octano para MODO

## Substance en el complemento MODO

Los resultados del Substance funcionan de forma nativa con Octane. Puede utilizar las siguientes salidas de Substance y configuraciones de efectos de capa de textura.

1. Cree un Substance > Textura > Crear Substance y defina el modo en Material irreal. El uso de material de Unreal le permitirá ver la textura en la ventana gráfica de Advanced OGL.
1. Cree salidas para color base, metálico, rugosidad y normal.
1. MODO utiliza mapas normales de OGL. En las propiedades del Substance, debe cambiar la dirección normal a OpenGL.

   ![](../../../assets/ogl.png)
1. Cargue el ajuste preestablecido de PBR del Substance. Este ajuste preestablecido es una modificación de octanos. Arrástrelo al grupo de sombreadores.

   [Substance\_PBR.lxp](https://helpx.adobe.com/content/dam/help/en/substance-3d/documentation/integrations/files/162005234/162005272/1/1502792782697/substance-pbr.lxp)
1. Seleccione la modificación y arrastre las salidas del Substance desde el Navegador de clips a la Vista de esquema. Tome el nodo con la salida del nombre de archivo y conéctelo al nodo de entrada apropiado, es decir, color base → color base.

   ![](../../../assets/connect-6.png)
1. Conectar el resto de las salidas del Substance

   ![](../../../assets/outputs-4.png){width="640px"}
