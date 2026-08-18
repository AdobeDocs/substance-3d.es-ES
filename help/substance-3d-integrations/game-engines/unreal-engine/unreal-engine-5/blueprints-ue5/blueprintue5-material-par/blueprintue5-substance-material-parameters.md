---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/blueprints-ue5/blueprintue5-substance-material-parameters.html"
breadcrumb-title: ''
description: Cambie los parámetros de material del Substance en tiempo de ejecución en Unreal Engine 5 mediante los nodos Blueprint para el control dinámico de materiales.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Blueprints - UE5 > Blueprint(UE5) Substance material parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Parámetros de material del Substance Blueprint(UE5)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---


# Modelo(UE5): Parámetros de material de Substance

## Cambiar un parámetro float:

Utilizará [Establecer nodo flotante de entrada](https://helpx.adobe.com/es/substance-3d/unlisted/documentation/integrations/blueprint-node-reference-151584784.html) para cambiar un flotante, color(float4) y parámetros booleanos de substance.

1. Cree una variable con un tipo de &quot;Instancia de Gráfico de Substance&quot; como referencia.\
   \**Para ello, agregue una variable en la ficha Mi plan y asígnele un nombre. En el menú desplegable, busque Instancia de Gráfico de Substance > Referencia de objeto. Arrastre la variable al gráfico y seleccione Obtener (nombre de variable). Establezca la instancia de Gráfico de Substance en la sección Valor predeterminado de la ficha Detalles.*
1. Cree un nodo flotante Set Input y establezca el destino como la variable Instancia de Gráfico de Substance. Es posible que la casilla Sensible al contexto de la ventana de búsqueda deba desactivarse para ver todos los resultados.
1. En el nodo flotante Definir entrada, establezca el identificador como el nombre del parámetro de Substance que se va a cambiar.\
   *\* Puede encontrar el nombre del identificador abriendo el Substance INST y pasando el ratón sobre el nombre del parámetro. El nombre del identificador aparecerá en la ventana emergente de información sobre herramientas.*
1. En el nodo flotante de entrada, arrastre una conexión y cree un nodo de matriz de creación. El nodo Make Array tendrá un índice de 0. El índice 0 corresponde al valor flotante.
1. Cree un nodo de procesamiento asíncrono o sincronizado y conecte la línea de ejecución del flotante de entrada definida al nodo de procesamiento. Establezca las instancias que se van a procesar en la variable de instancia de Gráfico de Substance.\
   *\* La sincronización asíncrona no es bloqueante y la sincronización lo es.*

![](../../../../../assets/steps.png){width="800px"}

## Parámetros booleanos

Los parámetros booleanos se cambian utilizando Set Input Bool.

![](../../../../../assets/setbool.png){width="800px"}

## Parámetros de color

Los parámetros de color se cambian mediante Definir color de entrada.

![](../../../../../assets/setcolor.png){width="800px"}

## Cambiar un parámetro Integer:

Los parámetros enteros funcionan igual que el valor de Set Input Float. Utilizará el nodo Set Input Integer.

![](../../../../../assets/int.png)

## Identificadores

Puede encontrar el identificador de un parámetro en la sustancia INST. Pase el ratón sobre el parámetro y la información sobre herramientas mostrará el nombre del identificador. Éste es el nombre definido en el campo identificador de la salida en Substance Designer.

![](../../../../../assets/screen-shot-2022-04-01-at-4-50-02-pm-copy.png)
