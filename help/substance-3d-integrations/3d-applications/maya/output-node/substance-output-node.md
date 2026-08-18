---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/3d-applications/maya/substance-output-node.html"
breadcrumb-title: ''
description: Entender cómo funcionan los nodos de salida Substance en maya para conectar texturas computadas a redes de sombreadores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Substance Output Node
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nodo de salida de Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Nodo de salida de Substance

El nodo de salida del Substance es una referencia a la textura calculada del Substance Engine. Está conectado al nodo Substance. Cuando se crea una salida en el nodo Substance, el motor Substance calcula la textura y estos datos se conservan en RAM. Si se utiliza el motor de GPU, los datos se calculan en GPU y se devuelven a la memoria mediante el motor de fusión de GPU de Substance. Las salidas del nodo Substance que no están activadas no se calculan.

![](../../../assets/outputnode.png)

En este nodo, puede ver la información de salida, como el identificador, la etiqueta y el uso establecidos en la salida de Substance Designer. Este nodo también le permite Convertir la textura en disco en la sección Almacenamiento en caché de resultados .
