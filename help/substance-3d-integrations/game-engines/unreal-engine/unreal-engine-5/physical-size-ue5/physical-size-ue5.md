---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/physical-size-ue5.html"
breadcrumb-title: ''
description: Usa la configuración del tamaño físico para escalar materiales del Substance en función de las dimensiones del mundo real en Unreal Engine 5.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Physical Size - UE5
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tamaño físico - UE5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Tamaño físico - UE5

El tamaño físico en materiales Substance permite escalar los materiales en función de su tamaño en el mundo. Este valor se establece en Substance Designer y se lee en Unreal a través del sistema de plantillas de materiales.\
El material [Substance\_Triplanar\_Template](../../../../game-engines/unreal-engine/unreal-engine-5/material-template-usage/out-the-box-material-tem/out-of-the-box-material-templates.md) del elemento principal contiene un ejemplo de cómo se puede usar el tamaño físico para escalar materiales irreales.



Independientemente de los valores de ampliación de la malla, los materiales se embaldosarán en función del tamaño que ocupan en el mundo en centímetros. En el caso del material rocoso (imagen 1), esto es 1,8 m (180 cm) para cada medida.

![](../../../../assets/rock-material-parameters.png)

Los materiales de Substance que contengan datos de tamaño físico tendrán sus valores copiados en cualquier nodo de parámetro vectorial de material existente denominado tamaño físico.



Como no hay ningún valor de desplazamiento en los materiales en UE5, la plantilla de tamaño físico copia el valor como X, Y, X para el mapa triplanar.
