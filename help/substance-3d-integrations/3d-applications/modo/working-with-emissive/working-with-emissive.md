---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/3d-applications/modo/working-with-emissive.html"
breadcrumb-title: ''
description: Configure las propiedades de emisión para los materiales de Substance en MODO para controlar la cantidad de luminosidad y los ajustes de color.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Working with Emissive
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trabajar con Emissive
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# Trabajar con Emissive

## Uso de Emissive (cantidad luminosa y color)

El Substance puede tener una salida de emisión opcional. Puede utilizar esta opción como Cantidad luminosa y Color en MODO. Al habilitar la salida de emisión, se establecerá en el efecto Cantidad luminosa. De forma predeterminada, este canal se interpreta como Lineal en la ficha Imagen de textura fija.\
Haga clic con el botón derecho en la textura del árbol del sombreador y seleccione Duplicar. A continuación, defina la textura emisiva duplicada en el efecto Color luminoso. A continuación, puede realizar cambios en los valores superior e inferior de la textura que activan el efecto Cantidad luminosa para intensificar aún más el valor.

>[!NOTE]
>
> Para que la textura se defina en Color luminoso, debe definir la interpretación en sRGB en la ficha Imagen fija.

Para obtener un efecto de floración, debe activar la floración en el panel Procesamiento y establecer el Umbral y el Radio.

![](../../../assets/bloom.png)

Para los materiales Unreal y Unity, el resultado Emissive se gestiona específicamente con el material.\
Irreal = Irreal Emisor\
Unidad = Emisión de unidad

Las texturas Emisión de irreal y Emisión de unidad deben cambiarse de Lineal a sRGB en la ficha Imagen fija.
