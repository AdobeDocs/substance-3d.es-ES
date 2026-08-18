---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/substance-3d-for-unity-scripting/class-documentation/substanceruntimegraph-class/member-function-documentation.html"
breadcrumb-title: ''
description: Documentación detallada de todas las funciones miembro de la clase SubstanceRuntimeGraph en scripts de Unity.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Substance 3D for Unity Scripting > Class Documentation > SubstanceRuntimeGraph Class > Member Function Documentation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Documentación de función de miembro
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 2%

---


# Documentación de función de miembro

## AttachGraph()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.AttachGraph  

( SubstanceGraphSO graph ) [inline]
```


Adjunta un nuevo objeto de gráfico a este controlador de tiempo de ejecución.

**Parámetros**

|  |  |
| --- | --- |
| graph | Gráfico de sustancia objetivo. |

### CreatePresetFromCurrentState()

```
string Adobe.Substance.Runtime.SubstanceRuntimeGraph.CreatePresetFromCurrentState ( ) [inline]
```


Guarda el estado actual del gráfico en un XML preestablecido.

**Devoluciones**

Ajuste preestablecido creado con el estado actual de las entradas del gráfico.

### GetGeneratedTextures()

```
List< Texture2D > Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetGeneratedTextures ( ) [inline]
```


Devuelve una lista con todas las texturas de salida para la instancia de substance.

**Devoluciones**

Textura de salida.

### GetInputBool()

```
bool Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputBool ( string inputName ) [inline]
```


Obtener entrada booleana del Substance.

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR. |


**Devoluciones**

Valor de entrada actual.

### GetInputColor()

```
Color Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputColor ( string inputName ) [inline]
```


Obtener color Substance

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |


**Devoluciones**

Valor de entrada actual.

### GetInputDescription()

```
SubstanceInputDescription Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputDescription ( string inputName ) [inline]
```


Devuelve la descripción de entrada completa del nombre de entrada de destino.

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de entrada de destino. |


**Devoluciones**

Descripción completa de la entrada de destino.

### GetInputFloat()

```
float Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputFloat ( string inputName ) [inline]
```


Obtener entrada flotante del Substance

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |


**Devoluciones**

Valor de entrada actual.

### GetInputInt()

```
int Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputInt ( string inputName ) [inline]
```


Obtener entrada de Substance

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |


**Devoluciones**

Valor de entrada actual.

### GetInputString()

```
string Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputString ( string inputName ) [inline]
```


Obtener entrada de cadena del Substance.

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |


**Devoluciones**

Introducir valor actual.

### GetInputVector2()

```
Vector2 Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputVector2 ( string inputName ) [inline]
```


Obtener entrada Vector2 de Substance

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |


**Devoluciones**

Valor de entrada actual.

### GetInputVector2Int()

```
Vector2Int Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputVector2Int ( string inputName ) [inline]
```


Obtener matriz de 2 int.

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |


**Devoluciones**

Valor de entrada actual.

### GetInputVector3()

```
Vector3 Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputVector3 ( string inputName ) [inline]
```


Obtenga la entrada Vector3 de Substance.

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |


**Devoluciones**

Valor de entrada actual.

### GetInputVector3Int()

```
Vector3Int Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputVector3Int ( string inputName ) [inline]
```


Obtener un conjunto de 3 int (valores x, y y z de Vector3Int)

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |


**Devoluciones**

Valor de entrada actual.

### GetInputVector4()

```
Vector4 Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputVector4 ( string inputName ) [inline]
```


Obtener entrada de vector4 de Substance

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |


**Devoluciones**

Valor de entrada actual.

### GetInputVector4Int()

```
int[] Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetInputVector4Int ( string inputName ) [inline]
```


Obtener un conjunto de 4 int (valores x, y, z y w de Vector4Int)

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |


**Devoluciones**

Valor de entrada actual.

### GetOutputTexture()

```
Texture2D Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetOutputTexture ( string outputName ) [inline]
```


Devuelve la textura de salida de un nombre de salida determinado.

**Parámetros**

|  |  |
| --- | --- |
| outputName | Nombre de salida. |


**Devoluciones**

Textura de salida.

### GetTexturesResolution()

```
Vector2Int Adobe.Substance.Runtime.SubstanceRuntimeGraph.GetTexturesResolution ( ) [inline]
```


Devuelve la resolución de salida de textura de instancia.

**Devoluciones**

Resolución de salida actual.

### HasInput()

```
bool Adobe.Substance.Runtime.SubstanceRuntimeGraph.HasInput ( string inputName ) [inline]
```


Devuelve verdadero si esta instancia de substance tiene una entrada con un nombre determinado.

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de entrada. |


**Devoluciones**

TRUE si la instancia de substance tiene una entrada con el nombre especificado.

### LoadPreset()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.LoadPreset ( string presetXML ) [inline]
```


Utiliza un XML preestablecido para definir los parámetros de entrada del gráfico.

**Parámetros**

|  |  |
| --- | --- |
| presetXML | Datos XML preestablecidos. |

### RenderAsync()

```
Task Adobe.Substance.Runtime.SubstanceRuntimeGraph.RenderAsync ( ) [inline]
```


Representa la instancia de substance de forma asincrónica.

**Devoluciones**

Tarea que finalizará una vez realizada la renderización.

### SetInputBool()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputBool ( string inputName, 

bool value ) [inline]
```


Entrada booleana del Substance de actualización

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |
| valor | Valor utilizado para actualizar el parámetro |

### SetInputColor()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputColor ( string inputName, 

Color value ) [inline]
```


Actualizar entrada de color del Substance

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |
| valor | Valor utilizado para actualizar el parámetro |

### SetInputFloat()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputFloat ( string inputName, 

float value ) [inline]
```


Actualizar entrada flotante del Substance

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |
| valor | Valor utilizado para actualizar el parámetro |

### SetInputInt()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputInt ( string inputName, 

int value ) [inline]
```


Actualizar entrada de entrada del Substance

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |
| valor | Valor utilizado para actualizar el parámetro |

### SetInputString()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputString ( string inputName, 

string value ) [inline]
```


Actualizar la entrada de cadena del Substance.

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |
| valor | Valor utilizado para actualizar el parámetro |

### SetInputTexture()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputTexture (string inputName, 

Texture2D value ) [inline]
```


Actualice Substance Texture2D Input.

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |
| valor | Valor utilizado para actualizar el parámetro |

### SetInputVector2()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputVector2 ( string inputName, 

Vector2 value ) [inline]
```


Actualizar entrada de vector2 del Substance

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |
| valor | Valor utilizado para actualizar el parámetro |

### SetInputVector2Int()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputVector2Int ( string inputName, 

Vector2Int value ) [inline]
```


Actualizar entrada Vector2Int del Substance.

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |
| valor | Valor utilizado para actualizar el parámetro |

### SetInputVector3()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputVector3 ( string inputName, 

Vector3 value ) [inline]
```


Actualizar entrada de vector3 del Substance

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |
| valor | Valor utilizado para actualizar el parámetro |

### SetInputVector3Int()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputVector3Int ( string inputName, 

Vector3Int value ) [inline]
```


Actualice La Entrada Vector3Int Del Substance.

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |
| valor | Valor utilizado para actualizar el parámetro |

### SetInputVector4()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputVector4 ( string inputName, 

Vector4 value ) [inline]
```


Actualizar entrada de vector4 del Substance

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |
| valor | Valor utilizado para actualizar el parámetro |

### SetInputVector4Int()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetInputVector4Int ( string inputName, 

int x, 

int y, 

int z, 

int w ) [inline]
```


Actualizar entrada Vector4Int del Substance

**Parámetros**

|  |  |
| --- | --- |
| inputName | Nombre de la entrada en SBSAR |
| x | Valor utilizado para actualizar el parámetro |
| y | Valor utilizado para actualizar el parámetro |
| z | Valor utilizado para actualizar el parámetro |
| w | Valor utilizado para actualizar el parámetro |

### SetTexturesResolution()

```
void Adobe.Substance.Runtime.SubstanceRuntimeGraph.SetTexturesResolution ( Vector2Int size ) [inline]
```


Establece la resolución de salida de la textura de instancia.

**Parámetros**

|  |  |
| --- | --- |
| talla |  |
