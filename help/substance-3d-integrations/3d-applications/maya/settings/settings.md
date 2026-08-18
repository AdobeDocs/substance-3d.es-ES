---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/3d-applications/maya/settings.html"
breadcrumb-title: ''
description: Configure los ajustes del plugin del Substance en Maya a través de la bandeja del Substance o el menú para personalizar el comportamiento.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Configuración
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---


# Configuración

Se puede acceder al menú de ajustes del Substance a través de la bandeja del Substance o el menú del Substance. La configuración de este menú se almacena en un archivo de configuración editable &quot;substance.cfg&quot;.

>[!NOTE]
>
> **Ubicaciones de archivo de configuración**
> 
> **Windows**:\
> C:\Users\\Documents\maya\\substance\\
> **MacOS**:\
> /Usuarios//Biblioteca/Preferences/Autodesk/maya//substance/\
> **Linux**:\
> /home//maya//substance/

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Resolución predeterminada

Establece la resolución predeterminada de un nodo de Substance cuando se carga el archivo sbsar.

## Flujo de trabajo de procesamiento

Establece el flujo de trabajo de procesamiento predeterminado que se utilizará en el nodo Substance.

## Motor de Substance

Configuración de preferencias específicas del Substance Engine y globales para todos los nodos del Substance. El motor Substance se utiliza para calcular las texturas del Substance.

### Tipo de motor

El Substance Engine está disponible como motor de CPU y GPU. Cambiar el motor requerirá reiniciar Maya. El motor de GPU permitirá resoluciones más altas que el motor de CPU.

>[!WARNING]
>
> Puede haber diferencias de cálculo entre la CPU y el motor de GPU, por lo que para obtener resultados uniformes, es mejor establecer el tipo con el mismo motor utilizado en Substance Designer.

Los núcleos de CPU y la memoria del motor son ajustes de la cantidad de recursos que el motor del Substance puede utilizar.

### Bloqueo de procesamientos

Esta opción le permite establecer si el equipo del motor del Substance bloqueará los procesos de la interfaz de usuario de Maya. Cuando se habilita, el motor Substance tiene prioridad y bloquea los procesos de la interfaz de usuario de Maya. Cuando se deshabilitan, los procesos de la interfaz de usuario de Maya no se bloquean mediante cálculos del motor del Substance.

## Almacenar en caché salidas en disco

Establece la ubicación de caché predeterminada, el tipo de archivo y la carpeta de caché para todos los nodos de Substance recién creados en un proyecto.

## Extensiones de procesamiento

Habilite Extensiones de procesamiento para utilizar salidas de Substance directamente con sombreadores de Arnold.

## Tamaño físico

Active si el Tamaño físico se debe usar de forma predeterminada cuando se cargan los archivos sbsar y si se debe volver a calcular al volver a cargar el sbsar.

</td>
<td style="border: 0;" valign="top">

![](../../../assets/settings-35.png)

</td>
</tr>
</table>
