---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/game-engines/unity/substance-3d-for-unity-scripting/class-documentation/substanceruntimegraph-class.html"
breadcrumb-title: ''
description: Documentación de referencia para la clase SubstanceRuntimeGraph utilizada para las operaciones de gráficos en tiempo de ejecución en Unity.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Substance 3D for Unity Scripting > Class Documentation > SubstanceRuntimeGraph Class
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Clase SubstanceRuntimeGraph
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 0%

---


# Clase SubstanceRuntimeGraph

## Adobe.Substance.Runtime.SubstanceRuntimeGraph Referencia de la clase

Clase que proporciona funcionalidad en tiempo de ejecución para modificar entradas y representar gráficos de sustancias, permitiendo al Substance · GraphSO generar sus recursos en tiempo de ejecución.

Diagrama de herencia de Adobe.Substance.Runtime.SubstanceRuntimeGraph:

![](../../../../../assets/image2022-10-14-17-53-23-1.png)

### Funciones de miembro públicas

```
• void AttachGraph (SubstanceGraphSO graph)
```


Adjunta un nuevo objeto de gráfico a este controlador de tiempo de ejecución.

```
• void SetInputFloat (string inputName, float value)
```


Actualizar entrada flotante del Substance

```
• float GetInputFloat (string inputName)
```


Obtener entrada flotante del Substance

```
• void SetInputVector2 (string inputName, Vector2 value)
```


Actualizar entrada de vector2 del Substance

```
• Vector2 GetInputVector2 (string inputName)
```


Obtener entrada Vector2 de Substance

```
• void SetInputVector3 (string inputName, Vector3 value)
```


Actualizar entrada de vector3 del Substance

```
• Vector3 GetInputVector3 (string inputName)
```


Obtenga la entrada Vector3 de Substance.

```
• void SetInputVector4 (string inputName, Vector4 value)
```


Actualizar entrada de vector4 del Substance

```
• Vector4 GetInputVector4 (string inputName)
```


Obtener entrada de vector4 de Substance

```
• void SetInputColor (string inputName, Color value)
```


Actualizar entrada de color del Substance

```
• Color GetInputColor (string inputName)
```


Obtener color Substance

```
• void SetInputBool (string inputName, bool value)
```


Entrada booleana del Substance de actualización

```
• bool GetInputBool (string inputName)
```


Obtener entrada booleana del Substance.

```
• void SetInputInt (string inputName, int value)
```


Actualizar entrada de entrada del Substance

```
• int GetInputInt (string inputName)
```


Obtener entrada de Substance

```
• void SetInputVector2Int (string inputName, Vector2Int value)
```


Actualizar entrada Vector2Int del Substance.

```
• Vector2Int GetInputVector2Int (string inputName)
```


Obtener matriz de 2 int.

```
• void SetInputVector3Int (string inputName, Vector3Int value)
```


Actualice La Entrada Vector3Int Del Substance.

```
• Vector3Int GetInputVector3Int (string inputName)
```


Obtener un conjunto de 3 int (valores x, y y z de Vector3Int)

```
• void SetInputVector4Int (string inputName, int x, int y, int z, int w)
```


Actualizar entrada Vector4Int del Substance

```
• int[ ] GetInputVector4Int (string inputName)
```


Obtener un conjunto de 4 int (valores x, y, z y w de Vector4Int)

```
• void SetInputString (string inputName, string value)
```


Actualizar la entrada de cadena del Substance.

```
• string GetInputString (string inputName)
```


Obtener entrada de cadena del Substance.

```
• SubstanceInputDescription GetInputDescription (string inputName)
```


Devuelve la descripción de entrada completa del nombre de entrada de destino.

```
• void SetInputTexture (string inputName, Texture2D value)
```


Actualice Substance Texture2D Input.

```
• Vector2Int GetTexturesResolution ()
```


Devuelve la resolución de salida de textura de instancia.

```
• void SetTexturesResolution (Vector2Int size)
```


Establece la resolución de salida de la textura de instancia.

```
• bool HasInput (string inputName)
```


Devuelve verdadero si esta instancia de substance tiene una entrada con un nombre determinado.

```
• List< Texture2D > GetGeneratedTextures ()
```


Devuelve una lista con todas las texturas de salida para la instancia de substance.

```
•  Texture2D GetOutputTexture (string outputName)
```


Devuelve la textura de salida de un nombre de salida determinado.

```
• void Render ()
```


Interpreta la instancia de substance de forma sincrónica.

```
• Task RenderAsync ()
```


Representa la instancia de substance de forma asincrónica.

```
• void LoadPreset (string presetXML)
```


Utiliza un XML preestablecido para definir los parámetros de entrada del gráfico.

```
• string CreatePresetFromCurrentState ()
```


Guarda el estado actual del gráfico en un XML preestablecido.

## Atributos públicos

```
• SubstanceGraphSO GraphSO
```


Instancia de sustancia de destino.

## Funciones de miembro protegidas

```
• void Awake ()
```


Al estar despierto, se utilizará SubstanceRuntime para crear una instancia para el SubstanceGraphSO adjunto en la sustancia

SDK.

```
• void Update ()
```


Compruebe el procesamiento de ConcurrentQueue para ver los resultados del procesamiento.

```
• void OnDestroy ()
```


Desecha el controlador de substance SDK.

## Propiedades

```
• Material DefaulMaterial [get]
```


Material principal generado por la instancia de substance.
