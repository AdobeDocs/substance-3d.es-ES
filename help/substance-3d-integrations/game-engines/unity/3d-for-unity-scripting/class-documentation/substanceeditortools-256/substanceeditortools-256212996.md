---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/substance-3d-for-unity-scripting/class-documentation/substanceeditortools-256212996.html"
breadcrumb-title: ''
description: Documentación de referencia para la clase SubstanceEditorTools utilizada para la administración de materiales de Substance en Unity.
helpx_creative_field: ""
helpx_description: Substance 3D Integrations
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SubstanceEditorTools
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---


# SubstanceEditorTools

## Adobe.SubstanceEditor.SubstanceEditorTools (Referencia de clases)

Herramientas y utilidades para que los usuarios las utilicen en secuencias de comandos de Editor.

Diagrama de herencia de Adobe.SubstanceEditor.SubstanceEditorTools:

![](../../../../../assets/image2022-10-14-17-53-23.png)

### Funciones de miembro públicas estáticas

```
• static void SetGraphFloatInput (SubstanceGraphSO graph, int inputId, float value)
```


Definir entrada flotante de gráfico.

```
• static void SetGraphFloat2Input (SubstanceGraphSO graph, int inputId, Vector2 value)
```


Defina la entrada de gráfico flotante2.

```
• static void SetGraphFloat3Input (SubstanceGraphSO graph, int inputId, Vector3 value)
```


Definir entrada de gráfico flotante3.

```
• static void SetGraphFloat4Input (SubstanceGraphSO graph, int inputId, Vector3 value)
```


Definir entrada float4 del gráfico.

```
• static void SetGraphIntInput (SubstanceGraphSO graph, int inputId, int value)
```


Definir entrada de gráfico int.

```
• static void SetGraphInt2Input (SubstanceGraphSO graph, int inputId, Vector2Int value)
```


Definir entrada de gráfico int2.

```
• static void SetGraphInt3Input (SubstanceGraphSO graph, int inputId, Vector3Int value)
```


Definir entrada de gráfico int3.

```
• static void SetGraphInt4Input (SubstanceGraphSO graph, int inputId, int value0, int value1, int value2, int value3)
```


Definir entrada int4 del gráfico.

```
• static void SetGraphInputString (SubstanceGraphSO graph, int inputId, string value)
```


Establecer la entrada de la cadena gráfica.

```
• static void SetGraphInputTexture (SubstanceGraphSO graph, int inputId, Texture2D value)
```


Defina la entrada de textura de gráfica.

```
• static void RenderGraph (SubstanceGraphSO graph)
```


Interpreta el gráfico de destino y actualiza sus recursos.

```
• static string CreatePresetFromCurrentState (SubstanceGraphSO graph)
```


Crea un XML preestablecido a partir del estado actual del objeto gráfico.

```
• static List< SubstanceGraphSO > GetGraphs (this SubstanceFileSO fileSO)
```


Devuelve la lista de SubstanceGraphSO asociados a un SubstanceFileSO.
