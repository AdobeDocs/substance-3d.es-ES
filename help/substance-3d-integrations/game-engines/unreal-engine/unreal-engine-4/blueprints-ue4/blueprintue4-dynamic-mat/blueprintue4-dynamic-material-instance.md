---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/blueprints-ue4/blueprintue4-dynamic-material-instance.html"
breadcrumb-title: ''
description: Crea instancias dinámicas de materiales a partir de materiales de Substance en tiempo de ejecución en Unreal Engine 4 mediante Blueprints.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Blueprints - UE4 > Blueprint(UE4) Dynamic Material Instance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Instancia dinámica de material del modelo (UE4)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---


# Modelo(UE4): Instancia dinámica de material

Puede crear una instancia de Gráfico de Substance para crear una instancia de gráfico dinámico en tiempo de ejecución.

1. Cree una variable de tipo Fábrica de instancias de Substance y establezca el valor predeterminado en Fábrica de Substance importada.
1. Añada un nodo Crear instancia de gráfico y conecte la fábrica de instancias de Substance a la entrada de fábrica. Establecer un nombre de instancia.
1. Cree otra variable de tipo Substance Instance Factory. Esto contendrá referencias al material de la sustancia dinámica.
1. Establezca la variable para el material de sustancia dinámico con el valor devuelto del nodo Crear instancia de gráfico.
1. Cree una variable de tipo Material. Esta será la plantilla de material. En el Navegador de contenido, cree un duplicado del material UE4 generado por el Substance. Establezca este material duplicado como la entrada para la variable de plantilla de material.
1. Añada una instancia de creación de material dinámico y defina la variable Plantilla de material como padre.

   ![](../../../../../assets/rt-01.png){width="800px"}
1. Cree una variable de tipo Material. Esta será la Dinámica de Instancias de Materiales (MID). Defina el valor devuelto de la instancia de material dinámico en la variable.

   ![](../../../../../assets/rt-02.png){width="800px"}
1. Añada un nodo de material definido y defina el valor de la variable MID como entrada de material. Para el destino, establézcalo en el objeto al que desea aplicar el material.
1. Cree una variable de tipo Name. Esta variable contendrá el nombre de los canales definidos en el material. Inicialice esto con el valor &quot;NONE&quot;
1. Agregue un nodo Obtener texturas de Substance y establezca la instancia de gráfico en la variable Instancia de gráfico dinámico.
1. Agregue un nodo For Loop. Aquí puede recorrer las texturas de Substance. Tome el resultado de Obtener texturas de Substance como matriz de entrada.

   ![](../../../../../assets/rt-03.png){width="800px"}
1. Agregue un nodo Substance Get Channel con el elemento array del bucle for como entrada.
1. Añada un nodo de secuencia. Aquí ejecutaremos primero el resultado del nodo Obtener canal.
1. Añada un conmutador en ESubChannelType después de Sequence Then 0 con el valor devuelto por Get Channel como Selection. Aquí comprobamos los nombres de los canales.
1. Establezca la variable MID Name en los nombres de canal del material de Substance duplicado del paso 5. *Ver la imagen de material.*
1. En el nodo Secuencia Entonces 1, configurará el proceso de asignación de los nombres de canal al material dinámico.
1. Obtener la variable de nombre MID y agregar un nodo de cadena igual con un valor de &quot;NONE&quot; Este es el valor inicializará la variable.
1. Agregue un nodo de bifurcación con la condición del nodo Igual.
1. Añada un valor de parámetro de textura de conjunto de Substance. El destino es la variable MID y el nombre del parámetro es la variable de nombre MID. Value es el elemento Array del nodo ForEachLoop.

![](../../../../../assets/material-1.png){width="800px"}
