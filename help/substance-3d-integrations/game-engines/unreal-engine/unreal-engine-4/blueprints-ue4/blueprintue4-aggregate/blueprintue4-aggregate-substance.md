---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/blueprints-ue4/blueprintue4-aggregate-substance.html"
breadcrumb-title: ''
description: Combina varios materiales de Substance en tiempo de ejecución en Unreal Engine 4 mediante nodos agregados de modelo para flujos de trabajo avanzados.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Blueprints - UE4 > Blueprint(UE4) Aggregate Substance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance agregado de modelo(UE4)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---


# Modelo(UE4): Substance agregado

El nuevo nodo de sustancia agregada le permite tomar dos fábricas de instancias de sustancia y crear una nueva fábrica de instancias en tiempo de ejecución que se puede utilizar para crear una nueva instancia de gráfico. Lo que hace que esto sea especial es que puede conectar texturas de salida de una de las instancias de gráficos combinadas a imágenes de entrada de la otra instancia de gráfico combinada. Para crear una instancia de gráficos de sustancias a partir de esta nueva fábrica, consulte nuestra documentación sobre instancias de gráficos de tiempo de ejecución. [Definición de instancia de material - UE4](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/material-instance-definition-157352129.html)

1. Importe los Substance que desee utilizar.
1. Cree una variable &quot;AggregateGraphInstance&quot; de tipo **Instancia de Gráfico de Substance**.
1. Cree una variable de tipo **Material** y **Dinámica de instancia de material**
1. Cree una **Conexión de Substance** y establezca los identificadores de entrada y salida.
1. Cree la **Fábrica de instancias de Substance agregado** y establezca la Fábrica de entrada y salida.
1. Cree una **instancia de gráfico** y establezca un nombre de instancia.
1. Establezca la variable **Instancia de gráfico agregado**.
1. Obtén texturas de sustancia desde la instancia de gráficos agregados en el paso 7 con **Obtener texturas de Substance**.
1. Cree una **instancia de material dinámico** utilizando la variable de material del paso 3 como principal.
1. Ajuste la variable MID del paso 3.
1. Establezca el material para la malla usando **Set Material** con la variable MID.

   ![](../../../../../assets/a2-3.png){width="800px"}
1. Establezca los canales para el material como se muestra en los documentos de instancias de materiales dinámicos (pasos 11-19)\
   [Modelo(UE4): Instancia de material dinámico](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/blueprint-dynamic-material-instance-152535142.html)

   ![](../../../../../assets/a4-3.png){width="800px"}
