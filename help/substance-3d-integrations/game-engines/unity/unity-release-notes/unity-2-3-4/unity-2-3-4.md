---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-3-4.html"
breadcrumb-title: ''
description: Revise las notas de la versión 2.3.4 del plugin Unity para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.3.4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.3.4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---


# Unity 2.3.4

>[!WARNING]
>
> **Si se usa el complemento con Unity 2019.2, se producirá el siguiente error:**
> 
> InspectorSubstanceImporter.OnInspectorGUI debe llamar a ApplyRevertGUI para evitar comportamientos inesperados.\
> UnityEditor.Experimental.AssetImporters.AssetImporterEditor:OnDisable()\
> Substance.Editor.InspectorSubstanceImporter:OnDisable()
> 
> Este error se puede borrar y no afectará a la funcionalidad del complemento

>[!WARNING]
>
> **Lea: Materiales de Substance que se rompen:**\
> Los materiales de Substance que contengan una salida personalizada con un uso en blanco se romperán al importarse. Además, los materiales de Substance que contengan usos duplicados se romperán.\
> Los archivos sbsar más antiguos de GameTextures.com no son compatibles actualmente con el plugin Substance en Unity. Estos materiales que contienen resultados de uso no compatibles se están rompiendo. Antes de usar el complemento, asegúrese de realizar una copia de seguridad del proyecto.

## Nuevas funciones:

* Se ha agregado la compatibilidad con Substance Engine v7
* Se ha agregado compatibilidad con Linux

### Correcciones de errores:

* Se han solucionado problemas relacionados con la importación de un Substance sin mapas de textura.
* Se ha corregido un problema por el que el proceso de reflexión no funcionaba correctamente en Unity 2019.x
* Se han solucionado problemas de gestión de prefabricados al importar un paquete que contenía prefabricados con materiales de Substance
* Asignaciones fijas de material/textura que no se arrastran después del proceso de reflexión
* Se ha solucionado un problema relacionado con el cambio de sombreados que provocaba la rotura de materiales.
* Se ha solucionado un problema por el que la rugosidad no se empaquetaba en el canal alfa metálico.
* Se ha solucionado un problema por el cual, al instalar el plugin de Substance, al cambiar la configuración de importación de texturas que no eran de Substance se revertían determinadas opciones.
* Se ha solucionado un problema por el que Substance Source no se abría en Mac.

## Problemas conocidos:

**Complemento del Substance principal**

* El usuario debe deshabilitar &quot;Habilitar Bitcode&quot; en el menú Configuración de compilación en Xcode para compilar para iOS
* Los Substance no trabajan con paquetes de recursos
* Los iconos de vista previa del Substance en el navegador de recursos cambian al icono del Substance S después de una reimportación
* Los materiales de Substance personalizados que tengan una salida con el uso definido en blanco romperán el material
* Los materiales de Substance personalizados que tengan usos duplicados romperán el material
* El editor debe reiniciarse después de importar el plugin en Linux

**Secuencias de comandos**

* Las secuencias de comandos no funcionan en tiempo de ejecución si el proyecto se establece en x86 en la configuración de generación
* Problemas al utilizar backend de scripts il2cpp con determinadas plataformas de compilación

**Substance Painter Live Link**

* Al crear un proyecto después de pintar con Substance Live Link, la malla pintada volverá al material predeterminado
* Canal AO no enviado con Painter Live Link
* Las mallas con varios materiales no funcionan en Unity Live Link
* La forma en que Unity LiveLink utiliza SimpleJson se bloquea con otras instancias de SimpleJson en un proyecto
