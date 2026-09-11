---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/features/tangent-space.html"
breadcrumb-title: ''
description: Descubre cómo los panaderos de Substance gestionan los cálculos de espacio tangente y personalizan el algoritmo para tu flujo de trabajo.
helpx_creative_field: ""
helpx_description: bakers > Features > Tangent Space
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Espacio tangente
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 1%

---


# Espacio tangente

Substance Bakers puede cargar las Tangentes y Binormales presentes en la malla de bajo contenido de poli o volver a calcularlas. Al volver a calcularlos es posible definir un algoritmo de Espacio de tangente personalizado (de forma predeterminada es MikkTSpace).

## Lista de complementos de Espacio de tangente

## Substance Painter

En Substance Painter, el complemento Tangent Space no se puede cambiar; siempre será **MikkTSpace**. Sin embargo, existe un parámetro para alterar ligeramente su comportamiento y hacerlo compatible con otras aplicaciones:

| *Parámetro* | *Compatible* *Aplicación* |
| --- | --- |
| **Calcular espacio tangente por fragmento: Deshabilitado** | Compatible con xNormal, Unity 5.3 o posterior. |
| **Calcular espacio tangente por fragmento: Habilitado** | Compatible con el flujo de trabajo de Unreal Engine 4, Blender y Unity HDRP. |

## Substance Designer

Substance Designer admite el siguiente algoritmo:

| *Nombre de archivo* | *Descripción* |
| --- | --- |
| **mikktspace.dll** | MikkTSpace, algoritmo de Espacio de tangente basado en el trabajo de Morten S. Mikkelsen.Compatible con xNormal, Unity 5.3 o posterior. |
| **mikkunrealtspace.dll** | MikkTSpace, algoritmo de Espacio de tangente basado en el trabajo de Morten S. Mikkelsen.Compatible con el flujo de trabajo de Unreal Engine 4, Blender y Unity HDRP. |
| **unitytspace.dll** | algoritmo de Espacio de tangente basado en Unity 4. |

>[!NOTE]
>
> Es posible escribir un plugin personalizado de Tangent Space. Hay un archivo de encabezado denominado **tangentspaceplugin.h** disponible en la carpeta de instalación en **Substance Designer/SDK/tangentspace** y que se puede usar como interfaz.

## Configuración de un Espacio de tangente personalizado

## Substance Painter

Substance Painter no admite complementos de Espacio de tangente personalizados en este momento. Esto significa que si Tangents y Binormals no están presentes en la malla de baja polimerización (utilizada para crear el proyecto) se recalcularán según el algoritmo de MikkTSpace.

## Substance Designer

Para definir el algoritmo de espacio tangente en Substance Designer, siga estos pasos:

1. Elija **Editar** > **Preferencias**.

   ![](../../assets/sd-edit-pref.png)
1. Haga clic en **Proyectos**.

   ![](../../assets/sd-pref-projects.png)
1. Vaya a la pestaña **General**. Desplácese hasta que la sección **Escenas 3D** esté visible.

   ![](../../assets/sd-tab-general.png)
1. Haga clic en los **tres puntos** (...) para cargar un complemento personalizado.

## Substance Automation Toolkit

Al hacer un bake con el conjunto de herramientas de automatización, es posible especificar el complemento Tangent Space con un argumento de línea de comandos específico:

```
sbsbaker normal-from-mesh --tangent-space-plugin "C:/Substance Designer/plugins⁄tangentspace⁄mikktspace.dll" ...
```
