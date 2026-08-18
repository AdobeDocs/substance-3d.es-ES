---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/3d-applications/blender/physical-size-in-blender.html"
breadcrumb-title: ''
description: Usa la configuración del tamaño físico para escalar materiales Substance según las dimensiones reales de Blender.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Blender > Physical size in Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tamaño físico en Blender
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---


# Tamaño físico en Blender

El tamaño físico en materiales Substance permite escalar los materiales en función de su tamaño en el mundo. Las dimensiones se establecen en aplicaciones de Substance como Designer y se muestran en la sección Tamaño físico del panel Complementos.

![](../../../assets/blender-physical-size.png)

Con el Tamaño físico activado, los materiales se embaldosarán en función de su tamaño real en centímetros. El mosaico de materiales permanecerá igual independientemente de la escala de los objetos. La función se puede activar cambiando al sombreador de Tamaño físico en el panel del complemento. Después de ajustar la escala de un objeto, la escala se debe aplicar con Ctrl/Cmd + A para estructurar con precisión la textura del Tamaño físico.

## Ajuste del Tamaño físico

Los valores del nodo de asignación se pueden ajustar para el control artístico sobre el mosaico de Tamaños físicos. Además, se puede utilizar un objeto, como Empty, para la entrada de Coordenadas de textura para controlar la asignación de textura mediante las transformaciones del objeto de entrada (consulte el ejemplo siguiente).

![](../../../assets/blender-physical-szie-empty.gif)
