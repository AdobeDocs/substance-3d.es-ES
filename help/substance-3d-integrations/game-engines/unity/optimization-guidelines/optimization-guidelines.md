---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/game-engines/unity/optimization-guidelines.html"
breadcrumb-title: ''
description: Siga las directrices de optimización para equilibrar la complejidad del material Substance con el rendimiento de procesamiento en Unity.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Optimization Guidelines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Directrices de optimización
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# Directrices de optimización

Cuanto más complejos sean los materiales del Substance, más potencia de procesamiento se necesitará para procesarlos. Por lo tanto, los materiales de Substance deben **encontrar un equilibrio entre la complejidad y la velocidad de procesamiento**. Esto es *especialmente* importante si se usarán en aplicaciones gráficas en tiempo real, como juegos.

Al crear sus propios materiales de Substance personalizados, asegúrese de comprobar las siguientes directrices de optimización.

[Directrices de optimización para Substance Designer](https://docs.substance3d.com/display/SDDOC/Performance+Optimization+Guidelines)

Una advertencia importante que debe tener en cuenta son los nodos que tienen una resolución absoluta de 4K o superior.

>[!WARNING]
>
> **Preste atención a la configuración de resolución y de resolución relativa a la principal.**\
> Los valores altos afectarán seriamente al rendimiento, por lo que debe tener en cuenta la probabilidad de uso del material y si puede reducir el tamaño de los datos involucrados.
>   
> El motor de CPU del Substance puede computar a 4K, pero es muy lento y puede hacer que una integración se bloquee o posiblemente se bloquee.

En el ejemplo siguiente, el tamaño de salida de un nodo [Tile Sampler](https://experienceleague.adobe.com/es/docs/substance-3d-designer/using/substance-graphs/nodes-reference-for-substance-graphs/node-library/texture-generators/patterns/tile-sampler) se establece en [Absolute](https://experienceleague.adobe.com/es/docs/substance-3d-designer/using/substance-graphs/output-size) 4096. Hace que varios nodos aguas abajo calculen a 4K antes de que se reduzcan para la resolución de salida final de 2048.

![](../../../assets/absolute.png){width="1000px"}
