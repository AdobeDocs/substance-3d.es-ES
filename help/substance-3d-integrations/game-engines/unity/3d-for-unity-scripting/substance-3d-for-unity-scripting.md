---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/game-engines/unity/substance-3d-for-unity-scripting.html"
breadcrumb-title: ''
description: Utilice la API de Substance 3D en Unity para escribir scripts que actualicen y cambien los parámetros del Substance en tiempo de ejecución.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Substance 3D for Unity Scripting
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Scripts de Substance 3D para Unity
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---


# Scripts de Substance 3D para Unity

Esta sección de la documentación contiene detalles sobre la API de Substance 3D que proporcionamos a través del plugin Substance 3D para Unity. Mediante las API de Substance, puede escribir secuencias de comandos para actualizar y cambiar los parámetros del Substance en tiempo de ejecución.

## Resumen de API

El plugin se divide en 3 conjuntos diferentes.

* Adobe.Substance
* Adobe.Substance.Editor
* Adobe.Substance.Runtime

### Adobe.Substance

Contiene componentes compartidos para interactuar con el SDK de Substance y generar objetos Unity coincidentes. También tiene estructuras de datos de cálculo de referencias para la comunicación entre C# y la API de C++ del SDK de Substance.

#### Adobe.Substance.Editor

Contiene clases específicas del editor para controlar la presentación de información sobre los objetos de Unity Substance, así como para controlar la canalización de importación para cuando se agregan archivos sbsar al proyecto. La clase SubstanceEditorEngine es un elemento único que controla la duración del motor de substance y todas sus instancias administradas.

#### Adobe.Substance.Runtime

Esta clase tiene componentes que controlarán la creación y administración de objetos Substance durante la ejecución en tiempo de ejecución. SubstanceRuntime es el equivalente de la clase SubstanceEditorEngine en tiempo de ejecución. Se ocupará de la inicialización del motor de substance, así como de la instanciación de cualquier instancia de substance con la que interactúen los scripts de usuario.

## Uso de tiempo de ejecución

Para que las entradas de la instancia del Substance se modifiquen en tiempo de ejecución, es necesario agregar un SubstanceRuntime←- Material a la escena (idealmente al mismo GameObject que el material de Substance). Esta clase actúa como ayudante para configurar el material mediante Adobe.Substance.Runtime.SubstanceRuntime singleton, que administra la creación de instancias de objetos SDK de Substance en tiempo de ejecución.

## Ejemplos de código

En el ejemplo siguiente se muestra cómo cambiar los parámetros de entrada en tiempo de ejecución mediante SubstanceRuntimeGraph.

### Cambio de parámetros

```
using System.Collections; 

using System.Collections.Generic; 

using UnityEngine; 

using Adobe.Substance.Runtime; 

public class scifiScript: MonoBehaviour { 

  public Adobe.Substance.Runtime.SubstanceRuntimeGraph mySubstance; 

  // Use this for initialization 

  void Start() { 

    UpdateSubstance(); 

  } 

  public void UpdateSubstance() { 

    // panel color 

    mySubstance.SetInputColor("paint_color", new Color(0.237 f, 0.834 f, 0.045 f, 1.0 f)); 

    // panel size 

    mySubstance.SetInputVector2("square_open", new Vector2(0.101 f, 0.209 f)); 

    // wear level 

    mySubstance.SetInputFloat("wear_level", 0.977 f); 

    // Submit async render. 

    mySubstance.RenderAsync(); 

  } 

}
```


También puede utilizar SubstanceRuntimeGraph para tener acceso a la información de entrada y salida sobre el material del Substance.

#### Obtener información de entrada

```
using System.Collections; 

using System.Collections.Generic; 

using UnityEngine; 

using Adobe.Substance.Runtime; 

public class scifiScript: MonoBehaviour { 

  public Adobe.Substance.Runtime.SubstanceRuntimeGraph mySubstance; 

  // Use this for initialization 

  void Start() { 

    UpdateSubstance(); 

  } 

  public void UpdateSubstance() { 

    SubstanceInputDescription desc = mySubstance.GetInputDescription("paint_color"); 

    Debug.Log($ "Input: {desc.Identifier}"); 

    Debug.Log($ "Index: {desc.Index}"); 

    Debug.Log($ "Type: {desc.Type}"); 

    Debug.Log($ "Label: {desc.Label}"); 

  } 

}
```


En el ejemplo siguiente se muestra cómo crear un menú de ajustes preestablecidos personalizado en el editor con SubstanceEditorTools.

##### Creación de controles preestablecidos.

```
using System.Collections; 

using System.Collections.Generic; 

using UnityEngine; 

using Adobe.Substance.Runtime; 

public class scifiScript: MonoBehaviour { 

  public Adobe.Substance.Runtime.SubstanceRuntimeGraph mySubstance; 

  // Use this for initialization 

  void Start() { 

    UpdateSubstance(); 

  } 

  public void UpdateSubstance() { 

    SubstanceInputDescription desc = mySubstance.GetInputDescription("paint_color"); 

    Debug.Log($ "Input: {desc.Identifier}"); 

    Debug.Log($ "Index: {desc.Index}"); 

    Debug.Log($ "Type: {desc.Type}"); 

    Debug.Log($ "Label: {desc.Label}"); 

  } 

}
```
