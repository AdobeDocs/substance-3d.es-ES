---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/blueprints-ue5/blueprintue5-aggregate-substance.html"
breadcrumb-title: ''
description: Combina varios materiales de Substance en tiempo de ejecución en Unreal Engine 5 mediante nodos agregados de Blueprint para flujos de trabajo avanzados.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Blueprints - UE5 > Blueprint(UE5) Aggregate Substance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance agregado de modelo (UE5)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---


# Modelo(UE5): Substance agregado

1. Utilice el nodo &quot;Crear fábrica de Substance agregados&quot; y establezca la fábrica de entrada y salida. La fábrica de salida debe tener un mapa de textura que se utilice como imagen de entrada en los parámetros de fábrica de entrada.
1. Cree objetos SubstanceConnection para cada textura de salida que se utilice como entrada con los nombres de los valores correspondientes (el nombre de salida del gráfico de salida y el nombre del parámetro de entrada del gráfico de entrada)
1. Añada un nodo Crear instancia de gráfico y conecte el resultado del nodo &quot;Crear fábrica de Substance agregados&quot; a la entrada de fábrica junto con un material principal para que actúe como plantilla (puede ser uno de los materiales predeterminados\_substance incluidos en el plugin).
1. Cree una variable Instancia de Gráfico de Substance y almacene el resultado del nodo anterior.
1. Opcional: Establezca los parámetros de sustancia que desee (en este ejemplo se establece una nueva resolución para las salidas de gráficos).
1. Cree un nodo de procesamiento asíncrono o de sincronización y conecte las instancias que se van a procesar a la variable de instancia de Gráfico de Substance.
1. Utilice la función &quot;Obtener instancia de material dinámica&quot; de la instancia de gráfico para crear u obtener una instancia de material existente. Si se deja vacío Nombre y En material padre, se utilizarán los parámetros utilizados al generar la instancia en el paso 3.
1. Añada un nodo de material definido y defina el valor de la variable MID como entrada de material. Para el destino, establézcalo en el objeto al que desea aplicar el material.
