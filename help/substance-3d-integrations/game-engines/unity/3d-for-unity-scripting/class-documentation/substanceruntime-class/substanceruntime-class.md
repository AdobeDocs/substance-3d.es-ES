---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/game-engines/unity/substance-3d-for-unity-scripting/class-documentation/substanceruntime-class.html"
breadcrumb-title: ''
description: Documentación de referencia para la clase SubstanceRuntime utilizada para las operaciones de material del Substance de tiempo de ejecución en Unity.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Substance 3D for Unity Scripting > Class Documentation > SubstanceRuntime Class
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Clase SubstanceRuntime
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 1%

---


# Clase SubstanceRuntime

## Adobe.Substance.Runtime.SubstanceRuntime (Referencia de clases)

Clase Singleton que controla la inicialización del motor del Substance y se utiliza para obtener controladores nativos para instancias de substance.\
Diagrama de herencia de Adobe.Substance.Runtime.SubstanceRuntime:

![](../../../../../assets/image2022-6-22-14-35-28.png)

### Funciones de miembro públicas

```
• SubstanceNativeGraph InitializeInstance (SubstanceGraphSO substanceInstance)
```


Crea un identificador de SDK de Substance para un SubstanceGraphSO determinado.

### Propiedades

```
• static SubstanceRuntime Instance [get]
```


Una instancia de Singleton.

### Descripción detallada

Clase Singleton que controla la inicialización del motor del Substance y se utiliza para obtener controladores nativos para instancias de substance.

### Documentación de función de miembro

#### InitializeInstance()

```
SubstanceNativeGraph Adobe.Substance.Runtime.SubstanceRuntime.InitializeInstance  

( SubstanceGraphSO substanceInstance ) [inline]
```


Crea un identificador de SDK de Substance para un SubstanceGraphSO determinado.

**Parámetros**

|  |  |
| --- | --- |
| substanceInstance | Target SubstanceGraphSO |


**Devoluciones**

Controlador que se comunica con el SDK del Substance

### Documentación de propiedad

#### Instancia

```
SubstanceRuntime Adobe.Substance.Runtime.SubstanceRuntime.Instance [static], [get]
```


Una instancia de Singleton.

Instancia singleton global.

>[!NOTE]
>
> NativeGraph.InRenderWork está diseñado únicamente para uso interno con el fin de comunicarse con el Substance Engine y no debe utilizarse para flujos de trabajo personalizados.
