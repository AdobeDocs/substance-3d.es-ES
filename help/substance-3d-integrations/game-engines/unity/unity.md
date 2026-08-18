---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity.html"
breadcrumb-title: ''
description: Importa y utiliza materiales de Substance en el motor de juegos Unity con compatibilidad con complementos nativos y control de parámetros de tiempo de ejecución.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unidad
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 0%

---


# Unidad

![](../../assets/unity.png)

>[!NOTE]
>
> **Versiones compatibles con Unity**
> 
> El complemento Substance 3D de Adobe para Unity versión 3.0.0 admite actualmente Unity 2020.3.27x y versiones superiores. Se puede descargar desde [Unity Asset Store](https://assetstore.unity.com/packages/tools/utilities/substance-3d-for-unity-beta-213208).

>[!WARNING]
>
> Antes de actualizar o usar el complemento, consulte la [página del proyecto de actualización](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/upgrading-projects-182256244.html).

>[!WARNING]
>
> Asegúrate de consultar la página [Directrices de optimización](../../game-engines/unity/optimization-guidelines/optimization-guidelines.md) antes de crear materiales personalizados para el Substance.

## Tabla de contenido

* [Notas de la versión de Unity](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/beta-release-information-170460277.html) — Novedades del plugin Substance in Unity por versión
* [Descargando el complemento Substance 3D en Unity](../../game-engines/unity/downloading-plugin-unity/downloading-substance-3d-plugin-in-unity.md): el Adobe Substance 3D para Unity está disponible en el almacén de recursos de Unity https://assetstore.unity.com/packages/tools/utilities/substance-in-unity-110555.
* [Descripción general del complemento Unity](../../game-engines/unity/unity-plugin-overview/unity-plugin-overview.md)
* [Preferencias de Unity](../../game-engines/unity/unity-preferences/unity-preferences.md): la ventana de preferencias del Substance le permite establecer opciones definidas por el usuario para el complemento.
* [Directrices de optimización](../../game-engines/unity/optimization-guidelines/optimization-guidelines.md): al crear tus propios materiales de Substance personalizados, asegúrate de comprobar las siguientes directrices de optimización.
* [Actualización de proyectos/problemas conocidos](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/upgrading-projects-182256244.html): problemas conocidos con el Substance en el complemento de Unity
* [Administración de Gráficos de Substance](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/managing-and-navigating-substance-graphs-170459636.html): puedes crear nuevos materiales basados en el material del Substance mediante el Administrador de Gráficos de Substance (SGM)
* [Cambio de parámetros](../../game-engines/unity/changing-parameters/changing-parameters.md): se puede acceder a los parámetros del material del Substance en el objeto de Gráfico de Substance (SGO).
* [Texturas generadas (Empaquetado)](../../game-engines/unity/generated-textures-pac/generated-textures-packing.md): las texturas generadas muestran las salidas del Substance calculadas por el Substance Engine para crear texturas
* [Espacio de color de procesamiento](../../game-engines/unity/rendering-color-space/rendering-color-space.md): para obtener los mejores resultados, debe establecer el espacio de color en lineal en la configuración del Reproductor de Unity.
* [Uso de entradas de imagen](../../game-engines/unity/using-image-inputs/using-image-inputs.md)
* [Publicación para dispositivos móviles](../../game-engines/unity/publishing-for-mobile/publishing-for-mobile.md) — Directrices para publicar en plataformas móviles
* [Secuencias de comandos de Substance 3D para Unity](../../game-engines/unity/3d-for-unity-scripting/substance-3d-for-unity-scripting.md): con la API de Substance, puede escribir secuencias de comandos para actualizar y cambiar los parámetros del Substance en tiempo de ejecución.
* [Secuencias de comandos en Unity (obsoleto)](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/scripting-in-unity-170459644.html): con la API de Substance, puede escribir secuencias de comandos para actualizar y cambiar los parámetros del Substance en tiempo de ejecución.
* [Uso de biblioteca de Substance 3D Assets](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/substance-3d-assets-library-225970070.html)
* [Eliminación del complemento Substance](../../game-engines/unity/removing-plugin/removing-substance-plugin.md)
* [Tutorials de Substance 3D en Unity](../../game-engines/unity/3d-in-unity-tutorials/substance-3d-in-unity-tutorials.md)
* [Tamaño físico en Unity](../../game-engines/unity/physical-size-in-unity/physical-size-in-unity.md)
* [Compartir archivos sbsar entre proyectos](https://helpx.adobe.com/sharing-sbsar-files-between-projects.html)[](../../game-engines/unity/sharing-sbsar-files-bet/sharing-sbsar-files-between-projects.md)

**[FORMULARIO ENCONTRADO: REGLAS OBLIGATORIAS]**

>[!WARNING]
>
> Antes de actualizar o usar el complemento, consulte la [página del proyecto de actualización](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/upgrading-projects-182256244.html).

>[!WARNING]
>
> Asegúrate de consultar la página [Directrices de optimización](../../game-engines/unity/optimization-guidelines/optimization-guidelines.md) antes de crear materiales personalizados para el Substance.

### Tabla de contenido

* [Notas de la versión de Unity](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/beta-release-information-170460277.html) — Novedades del plugin Substance in Unity por versión
* [Descargando el complemento Substance 3D en Unity](../../game-engines/unity/downloading-plugin-unity/downloading-substance-3d-plugin-in-unity.md): el Adobe Substance 3D para Unity está disponible en el almacén de recursos de Unity https://assetstore.unity.com/packages/tools/utilities/substance-in-unity-110555.
* [Descripción general del complemento Unity](../../game-engines/unity/unity-plugin-overview/unity-plugin-overview.md)
* [Preferencias de Unity](../../game-engines/unity/unity-preferences/unity-preferences.md): la ventana de preferencias del Substance le permite establecer opciones definidas por el usuario para el complemento.
* [Directrices de optimización](../../game-engines/unity/optimization-guidelines/optimization-guidelines.md): al crear tus propios materiales de Substance personalizados, asegúrate de comprobar las siguientes directrices de optimización.
* [Actualización de proyectos/problemas conocidos](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/upgrading-projects-182256244.html): problemas conocidos con el Substance en el complemento de Unity
* [Administración de Gráficos de Substance](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/managing-and-navigating-substance-graphs-170459636.html): puedes crear nuevos materiales basados en el material del Substance mediante el Administrador de Gráficos de Substance (SGM)
* [Cambio de parámetros](../../game-engines/unity/changing-parameters/changing-parameters.md): se puede acceder a los parámetros del material del Substance en el objeto de Gráfico de Substance (SGO).
* [Texturas generadas (Empaquetado)](../../game-engines/unity/generated-textures-pac/generated-textures-packing.md): las texturas generadas muestran las salidas del Substance calculadas por el Substance Engine para crear texturas
* [Espacio de color de procesamiento](../../game-engines/unity/rendering-color-space/rendering-color-space.md): para obtener los mejores resultados, debe establecer el espacio de color en lineal en la configuración del Reproductor de Unity.
* [Uso de entradas de imagen](../../game-engines/unity/using-image-inputs/using-image-inputs.md)
* [Publicación para dispositivos móviles](../../game-engines/unity/publishing-for-mobile/publishing-for-mobile.md) — Directrices para publicar en plataformas móviles
* [Secuencias de comandos de Substance 3D para Unity](../../game-engines/unity/3d-for-unity-scripting/substance-3d-for-unity-scripting.md): con la API de Substance, puede escribir secuencias de comandos para actualizar y cambiar los parámetros del Substance en tiempo de ejecución.
* [Secuencias de comandos en Unity (obsoleto)](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/scripting-in-unity-170459644.html): con la API de Substance, puede escribir secuencias de comandos para actualizar y cambiar los parámetros del Substance en tiempo de ejecución.
* [Uso de biblioteca de Substance 3D Assets](https://helpx.adobe.com/substance-3d/unlisted/documentation/integrations/substance-3d-assets-library-225970070.html)
* [Eliminación del complemento Substance](../../game-engines/unity/removing-plugin/removing-substance-plugin.md)
* [Tutorials de Substance 3D en Unity](../../game-engines/unity/3d-in-unity-tutorials/substance-3d-in-unity-tutorials.md)
* [Tamaño físico en Unity](../../game-engines/unity/physical-size-in-unity/physical-size-in-unity.md)
