---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/blueprints-ue5/blueprintue5-dynamic-material-instance-skip-to-end-of-metadata.html"
breadcrumb-title: ''
description: Crea instancias dinámicas de materiales a partir de materiales de Substance en tiempo de ejecución en Unreal Engine 5 mediante Blueprints.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Blueprints - UE5 > Blueprint(UE5) Dynamic Material Instance Skip to end of metadata
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Instancia de material dinámico del modelo (UE5) Ir al final de los metadatos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---


# Modelo(UE5): Instancia de material dinámico Ir al final de los metadatos

1. Cree una variable de tipo Fábrica de instancias de Substance y establezca el valor predeterminado en Fábrica de Substance importada.
1. Añada un nodo Crear instancia de gráfico y conecte la fábrica de instancias de Substance a la entrada de fábrica junto con un material principal para que actúe como plantilla (este puede ser uno de los materiales predeterminados de Substance incluidos en el plugin).
1. Cree otra variable para almacenar el objeto Instancia de Gráfico de Substance creado en el paso anterior.
1. Utilice la función &quot;Obtener instancia de material dinámica&quot; de la instancia de gráfico para crear u obtener una instancia de material existente. Si se deja vacío Nombre y En material padre, se utilizarán los parámetros utilizados al generar la instancia en el paso 2.
1. Cree una variable de tipo Material. Esta será la Dinámica de Instancias de Materiales (MID). Establezca el valor devuelto de &quot;Obtener instancia de material dinámico&quot; en la variable.

   ![](../../../../../assets/dynamic-material-annotated-1.png)
1. Añada un nodo de material definido y defina el valor de la variable MID como entrada de material. Para el destino, establézcalo en el objeto al que desea aplicar el material.
1. Opcional: Establezca los parámetros de sustancia que desee (en este ejemplo se utiliza una instancia de gráfico de sustancia preexistente y se copian los valores en la nueva).
1. Cree un nodo de procesamiento asíncrono o de sincronización y conecte las instancias que se van a procesar a la variable de instancia de Gráfico de Substance.
