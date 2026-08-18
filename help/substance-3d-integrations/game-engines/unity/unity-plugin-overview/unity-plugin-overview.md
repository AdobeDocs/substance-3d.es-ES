---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-plugin-overview.html"
breadcrumb-title: ''
description: Obtenga información sobre el complemento Substance 3D para Unity, incluidas la compatibilidad con versiones, funciones y capacidades de integración.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Plugin Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Descripción general del complemento Unity
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# Descripción general del complemento Unity

## Compatibilidad con versiones de Unity

La versión 3.0.0 del plugin Adobe Substance 3D para Unity admite actualmente Unity 2020 LTS y versiones superiores.

## Descarga del paquete de Substance

1. El complemento se puede descargar desde Unity Asset Store: <https://assetstore.unity.com/packages/tools/utilities/substance-3d-for-unity-beta-213208>

## Importación de un Material de Substance

1. Haga clic con el botón derecho del ratón en la ventana Proyecto y seleccione Importar recurso, o bien arrastre el material de Substance que desea importar al panel de vista del proyecto.
1. Busque el material del Substance que desea importar. Los materiales de Substance tienen la extensión de archivo &quot;.sbsar&quot;.
1. El material de Substance se importará en el proyecto de Unity.

   1. El recurso sbsar creará un archivo de importación principal y una carpeta que contendrá las texturas de salida y un material Unity generado.
1. A continuación, puede arrastrar y soltar el material en una malla en la vista de escena y, a continuación, editar los parámetros en el inspector.

   ![](../../../assets/window-overview.png){width="1000px"}

>[!NOTE]
>
> **Conversión de mapa normal**
> 
> El plugin Substance en Unity convierte automáticamente el DirectX a OpenGL. Al usar materiales de [Substance Source](https://source.substance3d.com/), no es necesario cambiar la orientación normal a OGL. Si va a crear su propio material en Substance Designer, asegúrese de trabajar con el sombreador de DirectX predeterminado, ya que el complemento se encargará de la conversión normal automáticamente. Para obtener más información, consulte Trabajar con normales en Unity.

## Cambio de parámetros

Los parámetros y las resoluciones se pueden definir en la ventana Inspector. Vea [Cambiar parámetros](../../../game-engines/unity/changing-parameters/changing-parameters.md).

[unity\_tweaking\_parameters.mp4](https://helpx.adobe.com/content/dam/help/en/substance-3d/documentation/download/attachments/186056716/unity-tweaking-parameters.mp4)

## Compatibilidad con canalizaciones de procesamiento de Unity

El complemento Substance 3D admite HDRP y URP. Pronto habrá más información disponible.

## Tutorial sobre cómo
