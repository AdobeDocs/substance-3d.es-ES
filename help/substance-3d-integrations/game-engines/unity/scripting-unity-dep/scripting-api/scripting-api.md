---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/game-engines/unity/scripting-in-unity-deprecated/scripting-api.html"
breadcrumb-title: ''
description: Documentación de referencia de la API de scripts obsoleta de Substance Unity para la compatibilidad con proyectos heredados.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Scripting in Unity (Deprecated) > Scripting API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: API de scripts
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '1074'
ht-degree: 1%

---


# API de scripts

## Substance en la API de Unity: 2.2.0

## Parámetros de material de Substance

| Método público | Descripción | Parámetro |
| --- | --- | --- |
| public **float** *GetInputFloat*(**string** inputName) | Obtener entrada **Float** del Substance | **Cadena** *inputName* Nombre de la entrada en SBSAR |
| public **int** *SetInputFloat*(**string** inputName, valor **float**) | Entrada **Float** del Substance de actualización | **Cadena** i *nombreEntrada* Nombre de la entrada en SBSAR **Float** *valor* Valor usado para actualizar el parámetro |
| public **void** *SetInputVector2*(**string** inputName, valor **Vector2**) | Actualizar la entrada del Substance **Vector2** | **Cadena** *inputName* Nombre de la entrada en SBSAR **Vector2** *input* Valores usados para actualizar el parámetro |
| public **vector2** *GetInputVector2*(**string** inputName) | Obtener entrada del Substance **Vector2** | **Cadena** &quot;inputName&quot; Nombre de la entrada en SBSAR |
| public **void** *SetInputVector3*(**string** inputName, valor **Vector3**) | Entrada del Substance de actualización **Vector3** | **Cadena** *inputName* Nombre de la entrada en SBSAR **Vector3** *valor* Valores usados para actualizar el parámetro |
| public **vector3** *GetInputVector3*(**string** inputName) | Obtener entrada del Substance **Vector3** | **Cadena** *inputName* Nombre de la entrada en SBSAR |
| public **void** *SetInputVector4*(**string** inputName, valor **Vector4**) | Entrada del Substance de actualización **Vector4** | **Cadena** *inputName* Nombre de la entrada en SBSAR **Vector4** *valor* Valores usados para actualizar el parámetro |
| public **vector4** *GetInputVector4*(**string** inputName) | Obtener entrada del Substance **Vector4** | **String** inputName Nombre de la entrada en SBSAR |
| public **void** *SetInputColor*(**string** inputName, valor **Color**) | Entrada de Update Substance **Color** | **String** inputName Nombre de la entrada en SBSAR **Color** Valor usado para actualizar el parámetro |
| public **color** *GetInputColor*(**string** inputName, **int** dataType) | Obtener Substance **Color** | **Cadena** *inputName* Nombre de la entrada en SBSAR **Int** *dataType* |
| public **void** *SetInputBool*(**string** inputName, valor **bool**) | Entrada **booleana** del Substance de actualización | **Cadena** *inputName* Nombre de la entrada en SBSAR **Bool** *value* Valor usado para actualizar el parámetro |
| public **bool** *GetInputBool*(**string** inputName) | Obtener entrada **Boolean** del Substance | **Cadena** *inputName* Nombre de la entrada en SBSAR |
| public **void** *SetInputInt*(**string** inputName, valor **int**) | Entrada **Int** Del Substance De Actualizaciones | **Cadena** *inputName* Nombre de la entrada en SBSAR **Int** *valor* Valor usado para actualizar el parámetro |
| public **int** *GetInputInt*(**string** inputName) | Obtener entrada **Int** Del Substance | **Cadena** *inputName* Nombre de la entrada en SBSAR |
| public **void** *SetInputVector2Int*(**string** inputName, **int** x, **int** y) | Actualizar la entrada del Substance **Vector2Int** | **Cadena** *inputName* Nombre de la entrada en SBSAR **Int** *x* Valor usado para actualizar el parámetro **Int** y Valor usado para actualizar el parámetro |
| **int[] Substance.Game.SubstanceGraph**.*GetInputVector2Int*( string inputName) | Obtener un conjunto de 2 int (valores x e y de Vector2Int) | **Cadena** *inputName* Nombre de la entrada en SBSAR **Int** *x* Valor usado para actualizar el parámetro **Int** y Valor usado para actualizar el parámetro |
| **void Substance.Game.SubstanceGraph**.*SetInputVector3Int*( string inputName, int x, int y, int z) | Actualizar entrada Vector3Int del Substance | **Cadena** *inputName* Nombre de la entrada en el SBSAR **Int** *x* Valor usado para actualizar el parámetro **Int** y Valor usado para actualizar el parámetro **Int** z Valor usado para actualizar el parámetro |
| **int[] Substance.Game.SubstanceGraph**.*GetInputVector3Int*( string inputName) | Obtener un conjunto de 3 int (valores x, y y z de Vector3Int) | **Cadena** *inputName* Nombre de la entrada en el SBSAR **Int** *x* Valor usado para actualizar el parámetro **Int** y Valor usado para actualizar el parámetro **Int** z Valor usado para actualizar el parámetro |
| **void Substance.Game.SubstanceGraph**.*SetInputVector4Int*( string inputName, int x, int y, int z, int w) | Actualizar entrada Vector4Int del Substance | **Cadena** *inputName* Nombre de la entrada en el SBSAR **Int** *x* Valor usado para actualizar el parámetro **Int** y Valor usado para actualizar el parámetro **Int** z Valor usado para actualizar el parámetro **Int** w Valor usado para actualizar el parámetro |
| **int[] Substance.Game.SubstanceGraph**.*GetInputVector4Int*( string inputName) | Obtener un conjunto de 4 int (valores x, y, z y w de Vector4Int) | **Cadena** *inputName* Nombre de la entrada en el SBSAR **Int** *x* Valor usado para actualizar el parámetro **Int** y Valor usado para actualizar el parámetro **Int** z Valor usado para actualizar el parámetro **Int** w Valor usado para actualizar el parámetro |
| **void Substance.Game.SubstanceGraph**.*SetInputString*( string inputName, string value) | Actualizar la entrada de cadena del Substance | **Cadena** *inputName* Nombre de la entrada en SBSAR **Cadena** *valor* usado para actualizar el parámetro |
| **string Substance.Game.SubstanceGraph**.*GetInputString*( string inputName) | Obtener entrada de cadena del Substance | **Cadena** *inputName* Nombre de la entrada en SBSAR |
| **void Substance.Game.SubstanceGraph**.*SetInputTexture*( string inputName, valor Texture2D) | Actualizar entrada de Substance Texture2D | **Cadena** *inputName* Nombre de la entrada en SBSAR **Texture2D** *value* usada para actualizar el parámetro |
| **Texture2D Substance.Game.SubstanceGraph**.*GetInputTexture*( string inputName) | Obtener entrada de Substance Texture2D | **Cadena** *inputName* Nombre de la entrada en SBSAR |
| **VectorInt Substance.Game.SubstanceGraph**.*GetTexturesResolution*() | Obtenga la resolución de texturas de Ajustes de destino del gráfico (los valores de Vector4Int x = ancho, y = height pueden ser 32, 64, 128, 256, 512, 1024, 2048 y 4096) | Ninguno |
| **int Substance.Game.SubstanceGraph**.*SetTexturesResolution*(Tamaño Vector2Int) | Establezca la resolución de texturas de Ajustes de destino del gráfico (Vector2: x = anchura, y = height, los valores pueden ser 32, 64, 128, 256, 512, 1024, 2048 y 4096) Devuelve 0 si es correcto; de lo contrario: -1. | **Vector2Int** *size* usado para actualizar el parámetro&#x200B;**.** |
| **List Substance.Game.SubstanceGraph**.*GetGeneratedTextures*() | Devuelve todos los objetos Texture2D del Substance utilizados por el sombreador de materiales del gráfico. | Ninguno |
| **int Substance.Game.SubstanceGraph**.*Bake*( Texture2D texture, string absolutePath) | Genere archivos .png para todos los objetos de Substance Texture2D utilizados por el sombreador de materiales del gráfico. | Ninguno |
| **&#x200B;**&#x200B;Substance.Game.**&#x200B; SubstanceGraph**.*Duplicate*() | Duplicar un Gráfico de Substance | Ninguno |
| **Substance.Game.SubstanceGraph**.*Duplicate*(string newGraphName) | Duplicar un Gráfico de Substance y asignarle un nombre (el material correspondiente también tendrá el mismo nombre) | **String newGraphName** |
| **&#x200B;**&#x200B;Substance.Game.**&#x200B; SubstanceGraph**.*GetInputProperties*() | Consulta información de entrada de procedimiento, devuelve una matriz de &#39;InputProperties&#39;, con:public struct InputProperties { nombre de cadena pública; // inputName public string label; // etiqueta del widget en el grupo de cadenas públicas de la GUI; // grupo del widget en GUIpublic string[] componentLabels; // para reguladores (hasta 4 etiquetas) cadena pública[] enumOptions; // para optionMenuPublic InputPropertiesType type;public Vector4 maximum; // para los reguladores públicos Vector4 mínimo; // para los reguladores de paso flotante público; // for sliders }public enum InputPropertiesType { Boolean = 0,// 0 Float, // 1 Vector2, // 2 Vector3, // 3 Vector4, // 4 Color, // 5 Enum, // 6 Texture, // 7 String, // 8 Invalid = -1/ -1 }; | Ninguno |
| **bool** **Substance.Game.SubstanceGraph**.*HasInput*(**string** inputName) | Compruebe si existe una entrada en un gráfico y devuelve verdadero/falso: | **Cadena** *inputName* Nombre de la entrada en SBSAR |
| **bool** **Substance.Game.SubstanceGraph**.*IsInputVisible*(**string** inputName) | Comprobar si una entrada visible es visible, devuelve verdadero/falso | **Cadena** *inputName* Nombre de la entrada en SBSAR |

## Renderizando

| Método público | Descripción | Parámetro |
| --- | --- | --- |
| public **void** *QueueForRender*() | Agregar gráfico de Substance a la cola | Ninguno |
| ***mySubstance.**&#x200B;RenderAsync()* | Renderizar todos los Substance en cola de forma asincrónica | Ninguno |
| ***mySubstance.**&#x200B;RenderSync()* | Renderizar todos los Substance en cola de forma sincrónica | Ninguno |

## Secuencias de comandos en modo Editor:

Para que las modificaciones de gráfica sean permanentes en el modo Editor, se debe realizar una reimportación de cada Substance correspondiente. Esto se hace con la siguiente función:

```
static void ReImportSubstance(Substance.Game.Substance pSubstance)

{



// Re-import Substance object:

SubstanceImporter importer = AssetImporter.GetAtPath(pSubstance.assetPath) as SubstanceImporter;

importer.CommitSubstanceToImporter(pSubstance); // plugin function

EditorUtility.SetDirty(importer);

importer.SaveAndReimport();



}
```


(con &quot;CommitSubstanceToImporter&quot;, una función de complemento de Substance: copiar todos los parámetros y/o entradas de gráfica modificados en el objeto importador de Substance, que se serializa en disco mediante el mecanismo importador de Unity)
