---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/material-template-usage-ue5.html"
breadcrumb-title: ''
description: Cree y utilice plantillas de material en Unreal Engine 5 para definir cómo se conectan los nodos de salida del Substance a las entradas de material.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Material Template Usage - UE5
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Uso de plantillas de material - UE5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# Uso de plantillas de material - UE5

Las plantillas de material permiten al usuario crear un material base para que los materiales se utilicen como plantilla para conectar sus nodos de salida a las entradas del material.\
Se utilizarán automáticamente las salidas que compartan el mismo nombre y tipo que una entrada de material. Este ejemplo de material principal tiene un nodo de muestra de textura &quot;baseColor&quot; que se rellenará si el Substance tiene una salida de textura denominada también &quot;baseColor&quot;.\
![](../../../../assets/parent-material-sample.png)

Las salidas de Substance admiten la actualización de texturas, valores escalares de tipo flotante único o int y valores vectoriales (2-4). Para utilizar resultados flotantes o int en tiempo de ejecución, debe obtener dynamicMaterialInstance del gráfico, ya que constanteMaterialInstances (cualquier material generado en el editor) no puede cambiar los valores escalares en tiempo de ejecución.

![](https://helpx-prod.scene7.com/is/image/HelpxProd/scalar-value?$png$&jpegSize=100&wid=245)

La instancia de substance graph intentará rellenar todos los valores de salida relevantes en el momento de la creación.

![](https://helpx-prod.scene7.com/is/image/HelpxProd/screen-shot-2022-04-01-at-4-38-31-pm?$png$&jpegSize=200&wid=1076)
