---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/maya/using-workflows.html"
breadcrumb-title: ""
description: Cree y utilice ajustes preestablecidos de procesamiento para las salidas del Substance en Maya para generar automáticamente redes de sombreador para diferentes procesadores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Using Workflows
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Uso de flujos de trabajo
user-guide-description: ""
user-guide-title: ""
source-git-commit: 28a9d8cf7a4eed4163f99e8158c9cb8f9da88302
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%
---

# Uso de flujos de trabajo

En Flujos de trabajo, puede elegir o crear ajustes preestablecidos de procesamiento para salidas de Substance. Estos ajustes preestablecidos son redes de sombreador para un procesador como Arnold o Vray.

>[!NOTE]
>
> **Ubicaciones preestablecidas de flujo de trabajo**
>
> **Windows**:
> C:\Users\\Documents\maya\2022\substance\workflows\generated
> **MacOS**:
> /Usuarios//Biblioteca/Preferences/Autodesk/maya//substance/workflows/generate
> **Linux**:
> /home/maya/substance/workflows/generate

![](../../../assets/maya-max-v3-1/maya-all-presets.png)

Para utilizar un flujo de trabajo, elija el ajuste preestablecido en la lista y, a continuación, haga clic en el botón Crear red.

![](../../../assets/workflow.gif)

## Creación de un flujo de trabajo

Puede crear su propio flujo de trabajo y agregarlo a la lista Flujo de trabajo del procesador. Al añadir un nuevo flujo de trabajo, cualquier nodo creado después del nodo Substance se guardará en el flujo de trabajo. Esto le permite crear cualquier número de nodos de sombreado para crear una red de sombreador personalizada completa que se pueda guardar como un flujo de trabajo preestablecido.

![](../../../assets/saved-workflow.png)

## Gestión de flujos de trabajo

### Guardar flujos de trabajo personalizados

1. Cree manualmente salidas de Substance y conéctelas a un material como aiStandardSurface.
   1. Puede usar cualquier Maya o renderizar nodos específicos para construir la red de sombreador.
1. Haga clic en el botón **Crear flujo de trabajo** e introduzca un nombre para el ajuste preestablecido de flujo de trabajo.

### Duplicación de flujos de trabajo

Puede duplicar un flujo de trabajo haciendo clic en el botón **Duplicar flujo de trabajo**.

### Cambiar nombre y sobrescribir flujos de trabajo

Puedes cambiar el nombre de los flujos de trabajo existentes, así como sobrescribir los flujos de trabajo con datos actualizados, utilizando los botones seleccionados **Cambiar nombre** y **Sobrescribir**.

### Eliminación de flujos de trabajo

Puede eliminar los flujos de trabajo existentes con el botón Quitar flujo de trabajo.

## Flujos de trabajo de OpenPBR

Hay dos flujos de trabajo de OpenPBR disponibles en la lista Flujos de trabajo: **OpenPBR** y **OpenPBR - V-Ray**. Estos flujos de trabajo están diseñados para usarse con archivos SBSAR creados mediante el modelo de material OpenPBR en Substance 3D Designer o Sampler (OpenPBR ha sido el modelo predeterminado desde Designer V16.0 y Sampler V6.0 y posteriores).

### Qué es el OpenPBR

OpenPBR es un modelo de sombreado de materiales abierto y basado en la física desarrollado por Adobe y Autodesk y que ha contribuido a la Academy Software Foundation (ASWF). Proporciona una definición de material unificada y compatible con todos los procesadores. Para obtener más información, visite la [documentación del OpenPBR](https://experienceleague.adobe.com/en/docs/substance-3d/general-knowledge/openpbr/openpbr-overview).

### Cuándo utilizar un flujo de trabajo de OpenPBR

Utilice un flujo de trabajo de OpenPBR cuando el archivo SBSAR se haya creado mediante el modelo de material de OpenPBR en Substance 3D Designer o Substance 3D Sampler. Si el SBSAR se ha creado utilizando el modelo de material estándar de Adobe (ASM), utilice el flujo de trabajo heredado compatible con su procesador (Arnold, V-Ray o V-Ray 6).

>[!NOTE]
>
> Si aplica un flujo de trabajo de OpenPBR a un material de ASM o un flujo de trabajo estándar a un SBSAR de OpenPBR, el plugin solo conectará las salidas que sean comunes a ambos modelos de material. El resultado puede ser incompleto.

### Flujos de trabajo de OpenPBR disponibles

**OpenPBR**

Utiliza el nodo maya nativo openPBRSurface. Compatible con Arnold y V-Ray. Este es el flujo de trabajo recomendado para la mayoría de los usuarios que trabajan con materiales de OpenPBR en maya.

**OpenPBR - V-Ray**

Utiliza el material V-Ray (VRayMtl) en modo OpenPBR. Recomendada para usuarios cuya canalización esté específicamente diseñada en torno a configuraciones de materiales V-Ray.

### Cómo aplicar un flujo de trabajo de OpenPBR

1. Cargue el archivo SBSAR en el complemento mediante el botón Cargar Substance .
1. En la lista Flujos de trabajo, seleccione **OpenPBR** o **OpenPBR - V-Ray**.
1. Haga clic en **Crear red** para crear la red de sombreador en el **Editor de materiales de hipersombra**.
1. El plugin conecta automáticamente las salidas SBSAR a las entradas correspondientes del nodo OpenPBR.
1. Asigne el material a la malla de la forma habitual.

![](../../../assets/maya-max-v3-1/maya-openpbr-overview.png)
