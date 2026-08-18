---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/renderers/corona/corona-for-3ds-max.html"
breadcrumb-title: ''
description: Utilice materiales Substance con el procesador Corona en 3ds Max mediante el flujo de trabajo Specular/Brillo y los mapas necesarios.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Corona > Corona for 3ds Max
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Corona para 3ds Max
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---


# Corona para 3ds Max

## Substance en Maya Plugin

![](../../../assets/scene-001v03.jpg)

## Corona 1.6 - 6

Con el [plugin 3ds Max](../../../3d-applications/3ds-max/3ds-max.md), puedes elegir Corona en el menú Substance para configurar automáticamente el material Corona con entradas de textura Substance.

![](../../../assets/corona.png){width="500px"}

## Corona 7 - 9

Para el procesamiento de Corona 7 y superior, al seleccionar &quot;Substance a Corona&quot; con el nodo Substance2 seleccionado, se creará una red para el material físico de Corona.

![](https://helpx-prod.scene7.com/is/image/HelpxProd/corona-physical-material?$png$&jpegSize=200&wid=857)

* **LiftGamaGain** se crea entre la salida de color base y la entrada de color base. Se utiliza un valor de gamma de 0,455 para corregir la diferencia de color.
* Se crea **CoronaNormal** entre la salida Normal y la entrada de relieve Base, así como entre la salida Normal Coat y la entrada Clearcoat Bump. No se cambia la configuración, pero aquí se pueden realizar modificaciones para la configuración normal.
* **CoronaMix** se crea entre la salida de Color de brillo y la entrada de Color de brillo. Se establece una cantidad de mezcla de 0 y un multiplicador de 2 para la capa base. Los usuarios pueden ajustar el valor Cantidad de mezcla para controlar el brillo.
