---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/3d-applications/modo/custom-materials.html"
breadcrumb-title: ''
description: Usa materiales personalizados Unreal, Unity y glTF en MODO con el plug-in de Substance para flujos de trabajo especializados.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Custom Materials
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Materiales personalizados
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 12%

---


# Materiales personalizados

El plugin de Substance es compatible con los materiales personalizados Unreal, Unity y glTF. Antes de cargar un archivo sbsar, puede seleccionar el modo de sombreado que desea utilizar.

## Tabla de contenido

## Material de Unity

Cuando se utiliza el material de Unity, el efecto de capa de material se configura automáticamente. El complemento Substance colocará el material Unity directamente encima del material del artículo Substance.

| Salida de Substance | Espacio de color | Efecto de capa de material |
| --- | --- | --- |
| Color base | sRGB | Albedo Unity |
| Brillo | Lineal | Smoothness Unity |
| Metálico | Lineal | Unity Metallic |
| Normal | Lineal | Unidad normal |
| Emisivo | sRGB | Emisión de unidad **\*establecida en sRGB en imagen fija** |
| Altura | Lineal | Bump de unidad |
| Oclusión ambiental | Lineal | Unity Ambient Oclusión |

![](../../../assets/unity-1.png){width="600px"}

## Material irreal

Al utilizar el material irreal, el efecto de capa de material se define automáticamente. El plug-in del Substance colocará el material irreal directamente encima del material del artículo del Substance.

| Salida de Substance | Espacio de color | Efecto de capa de material |
| --- | --- | --- |
| Color base | sRGB | Color base irreal |
| Rugosidad | Lineal | Rugosidad irreal |
| Metálico | Lineal | Metálico irreal |
| Normal | Lineal | Normal irreal |
| Altura | Lineal | Rugosidad irreal |
| Emisivo | sRGB | Emisivo irreal **\*establecido en sRGB en imagen fija** |
| Oclusión ambiental | Lineal | Oclusión ambiental irreal |
| Opacidad | Lineal | Opacidad irreal **\*debe desmarcar invertida en la capa de textura** |

![](https://helpx-prod.scene7.com/is/image/HelpxProd/unreal?$png$&jpegSize=200&wid=1343){width="600px"}

Es posible que tengas que invertir la normalidad. Puede hacerlo desde el menú Ajustes si el Substance tiene un control de orientación normal. Si no, esto se puede hacer en la propia textura. Para obtener más información, consulte la página &quot;**[Trabajando con normales](../../../3d-applications/modo/working-with-normals/working-with-normals.md)**&quot;.

## glTF Material

Al utilizar el material glTF, el efecto de capa de material se define automáticamente. El plugin del Substance colocará el material glTF directamente encima del material del artículo del Substance.

| Salida de Substance | Espacio de color | Efecto de capa de material |
| --- | --- | --- |
| Color base | sRGB | glTF Color base |
| Rugosidad | Lineal | Rugosidad glTF |
| Metálico | Lineal | glTF metálico |
| Normal | Lineal | glTF normal |
| Emisivo | sRGB | glTF emisivo **\*establecido en sRGB en imagen fija** |
| Oclusión ambiental | Lineal | glTF Oclusión ambiental |

![](../../../assets/gltf.png){width="600px"}

Es posible que tengas que invertir la normalidad. Puede hacerlo desde el menú Ajustes si el Substance tiene un control de orientación normal. Si no, esto se puede hacer en la propia textura. Para obtener más información, consulte la página &quot;**[Trabajando con normales](../../../3d-applications/modo/working-with-normals/working-with-normals.md)**&quot;.
