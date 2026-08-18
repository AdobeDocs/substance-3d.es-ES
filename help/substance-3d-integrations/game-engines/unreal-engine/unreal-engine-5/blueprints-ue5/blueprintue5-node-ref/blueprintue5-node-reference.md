---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/blueprints-ue5/blueprintue5-node-reference.html"
breadcrumb-title: ''
description: Guía de referencia para todos los nodos de Substance Blueprint disponibles en Unreal Engine 5 para operaciones de materiales.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Blueprints - UE5 > Blueprint(UE5) Node Reference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Referencia del nodo Blueprint(UE5)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 0%

---


# Modelo(UE5): Referencia de nodo

## Nodos de Substance general:

| Nombre | Entradas | Descripción |
| --- | --- | --- |
| **GetSubstances** | Entrada: **Material** | Devuelve una matriz de instancias de Gráfico de Substance utilizadas por un material. Si crea un material que utiliza salidas de textura de dos instancias gráficas diferentes, esta función devolverá esas dos instancias gráficas. |
| **GetSubstanceTextures** | Entrada: **SubstanceGraphInstance** | Devuelve una matriz de todas las texturas habilitadas y calculadas actualmente a partir del parámetro de entrada Instancia de Gráfico de Substance. |
| **GetGraphName** | Entrada: **SubstanceGraphInstance** | Devuelve el nombre del gráfico como se ha definido en Designer. |
| **GetFactoryName** | Entrada: **SubstanceGraphInstance** | Devuelve el nombre de **GraphInstanceFactory** que se utilizó para crear **SubstanceGraphInstance** que se pasa a este nodo. |
| **GetSubstanceLoadingProgress** | NINGUNO | Devuelve un flotador entre 0 y 1 con el porcentaje de cuántas sustancias se han cargado completamente. |
| **CreateGraphInstance** | Entrada: **SubstanceInstanceFactory**: el generador desde el que desea crear una instancia de gráfico.Entrada: **GraphIndex** (int): el índice del gráfico que desea crear. Entrada: **InstanceName** (FString): el nombre que desea que tenga la nueva instancia. | Devuelve una nueva instancia de gráfico independiente que se mantendrá hasta que se cierre la aplicación. |
| **DuplicateGraphInstance** | **SubstanceGraphInstance**: la instancia de gráfico de la que desea crear una copia. | Devuelve una nueva instancia de gráfico independiente que se mantendrá hasta que se cierre la aplicación. |
| **EnableInstanceOutputs** | Entrada: **SubstanceGraphInstance**: la instancia de gráfico que contiene el resultado para habilitar Input: **OutputIndices** (matriz int32): los índices de las salidas que desea habilitar. | Si se deshabilitó anteriormente, crea los resultados de textura de pasados en **SubstanceGraphInstance**. Esto tiene la misma funcionalidad que habilitar el resultado desde el editor **SubstanceGraphInstance**. *NOTA: Esto no actualizará el material con la textura recién creada. Esto se debe controlar estableciendo un parámetro de muestra en tiempo de ejecución mediante el nuevo resultado.* |
| **DeshabilitarResultadosDeInstancia** | Entrada: **SubstanceGraphInstance**: la instancia de gráfico que contiene el resultado para deshabilitar Input: **OutputIndices** (matriz int32): los índices de las salidas que desea deshabilitar | Si se activa, se desactivará y se eliminará la salida de textura del objeto de gráfico pasado |
| **CopyInputParameters** | Entrada: **SubstanceGraphInstance**: la instancia de gráfico a la que desea aplicar valores a Input: **SubstanceGraphInstance**: la instancia de gráfico de la que desea obtener los valores | Restaura todos los valores de entrada modificados del parámetro de entrada Instancia de Gráfico de Substance. |
| **ResetInputParameters** | Entrada: SubstanceGraphInstance | Restablecer los valores de entrada de una instancia de Gráfico de Substance a sus valores predeterminados |
| **SetGraphInstanceOutputSize** | Entrada: **SubstanceGraphInstance** Entrada: Anchura - Resolución de textura de la coordenada Xentrada: Height - Resolución de textura de la coordenada Y | Define la resolución de textura de todas las salidas generadas a partir de esta instancia de gráfico con los tamaños transferidos desde los parámetros. Nota: 2048 máx. en el motor de CPU Nota: 4096 máx. en el motor de GPU |
| **Procesamiento asíncrono** | **SubstanceGraphInstance** | Vuelve a calcular las texturas de salida de la entrada de instancia de Gráfico de Substance. (Sin bloqueo) |
| **SyncRendering** | **SubstanceGraphInstance** | Vuelve a calcular las texturas de salida de la entrada de instancia de Gráfico de Substance. (Bloqueo) |

## Funciones específicas de la instancia de gráfico:

Solo se puede llamar desde una instancia de gráfico

| Nombre | Entrada | Descripción |
| --- | --- | --- |
| GetDynamicMaterialInstance | Entrada: Nombre (cadena) | Devuelve la instancia de material dinámico en tiempo de ejecución de una sustancia o crea una si no existe. Las instancias de materiales dinámicos son necesarias para la mayoría de los cambios de valor de tiempo de ejecución de las salidas de valor de substance. |
| **GetInputNames** | NINGUNO | Devuelve una matriz de Strings que contiene todos los nombres de parámetros de entrada. |
| **GetInputType** | NINGUNO | Devuelve el tipo de datos asociado a esta entrada. |
| **SetInputInt** | Entrada: **Identificador** (cadena)Entrada: **InputValues** (matriz int) | Cambie el valor de una entrada encontrada por el identificador. Dentro de un juego, debe procesar la sustancia con **AyncRender** o **SyncRender** para que se apliquen los cambios. |
| **SetInputFloat** | Entrada: **Identificador** (cadena)Entrada: **InputValues** (matriz flotante) | Cambie el valor de una entrada encontrada por el identificador. Dentro de un juego, debe procesar la sustancia con **AyncRender** o **SyncRender** para que se apliquen los cambios. |
| **GetInputInt** | Entrada: **Identificador** (cadena) | Devuelve una matriz de puntos con los valores actuales de un parámetro de entrada. |
| **GetInputFloat** | Identificador (cadena) | Devuelve una matriz de valores flotantes con los valores actuales de un parámetro de entrada. |
| **SetInputBool** | Entrada: **Bool** (booleano)Entrada: **Identificador** (cadena) | Acepta un valor booleano para asignar un tipo de valor de entrada conmutable. Anteriormente, esto solo se podía lograr estableciendo un valor int de 1 o 0, que se convertiría en bool. |
| **GetInputBool** | Entrada: **Identificador** (cadena) | Devuelve el valor booleano actual de una entrada. |
| **SetInputColor** | Entrada: **Color** (LinearColor)Entrada: **Identificador** (FString) | Acepta un valor FLinearColor para asignar un tipo de valor de entrada de color a. Anteriormente, esto solo era alcanzable estableciendo un valor flotante y pasando una serie de valores flotantes. |
| **GetInputColor** | Entrada: Identificador (FString) | Devuelve el valor de color actual en formato UE4. |
| **CreateAggregateSubstanceFactory** | Entrada: **Fábrica de salida** (SubstanceInstanceFactory)*Fábrica que crea las salidas que se utilizarán como entrada en la fábrica de entrada.* Entrada: **Índice gráfico de fábrica de salida** (entero)*Qué gráfico de la sustancia desea usar para combinar.* Entrada: **Fábrica de entrada** (SubstanceInputFactory)*Fábrica que utiliza las salidas como imágenes de entrada de la fábrica de salida.*Entrada:**Conexiones**(Matriz de SubstanceConnections)*Esto se puede crear usando el nodo de plano Make Array. Una conexión de Substance es la forma en que se puede cambiar el nodo agregado que proporciona entradas para vincular a qué salidas.* **&#x200B; Return (SubstanceInstanceFactory)***Se puede usar para crear una instancia de gráfico de la nueva instancia combinada.* | El nuevo nodo de sustancia agregada permite tomar dos fábricas de instancias de sustancia y crear una nueva fábrica de instancias en tiempo de ejecución, que se puede utilizar para crear una nueva instancia de gráfico. Lo que hace que esto sea especial es que puede conectar texturas de salida de una de las instancias de gráficos combinadas a imágenes de entrada de la otra instancia de gráfico combinada. Para crear una instancia de gráficos de sustancias a partir de esta nueva fábrica, consulte nuestra documentación sobre instancias de gráficos de tiempo de ejecución. |
| **SubstanceConnectionStruct** | Entrada: **Identificador de salida** (FString)*El identificador de la textura de salida para encadenar en una entrada.* Entrada: **Identificador de entrada** (FString) | Lo utiliza Create Aggregate Substance Factory para especificar cómo encadenar cada textura de salida con nuevas texturas de entrada. |
