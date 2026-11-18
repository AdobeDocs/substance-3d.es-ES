---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/3d-applications/3ds-max/substance-in-3ds-max-overview.html"
breadcrumb-title: ""
description: Obtenga más información sobre el plugin Substance para 3ds Max y cómo importar y utilizar materiales de Substance en sus proyectos.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > Substance in 3ds Max Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Descripción general de Substance en 3ds Max
user-guide-description: ""
user-guide-title: ""
source-git-commit: 28a9d8cf7a4eed4163f99e8158c9cb8f9da88302
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 0%
---

# Descripción general de Substance en 3ds Max

## Descripción del complemento

## Abrir un Substance

1. Abra el Editor de pizarra, busque Substance y arrastre el nodo Substance2 a la vista.
1. Haga doble clic en el nodo Substance para activar las propiedades y, en Explorador de paquetes de Substance, cargue un Substance.

   >[!NOTE]
   >
   > También puede arrastrar y soltar el archivo .sbsar en el Editor de pizarra para crear automáticamente el nodo e importar la barra de pizarra.

1. Si un Substance contiene varias gráficas, puede elegir la gráfica que desea generar como material en el menú desplegable Gráfica seleccionada.

   ![](../../../assets/max1.png)

1. Con el nodo Substance seleccionado, vaya al menú Substance y elija un procesador compatible. El material se creará y estará listo para aplicarse al objeto. Las texturas de Substance se enlazan al material de procesamiento.

>[!NOTE]
>
> Una vez seleccionado el nodo **&quot;Substance2&quot;**, debe hacer clic primero en **Cargar Substance...** para seleccionar un archivo sbsar y, a continuación, seleccione un procesador compatible en el menú superior (p. ej. &quot;Substance de Arnold&quot;).
>
>Los renderizadores compatibles son Arnold, V-Ray, Corona y Octane. [Obtenga información sobre los flujos de trabajo en 3DS Max para saber cómo usar los materiales de OpenPBR.](../using-workflows-3ds-max/using-workflows-in-3ds-max.md)

![](../../../assets/max3.png)

## Cambio de resolución

1. Establezca la resolución deseada para las texturas calculadas del Substance en Ajustes de salida del Substance.
1. Para obtener una resolución de hasta 8 K, asegúrese de que está utilizando el motor de GPU, que se establece en [Configuración de Substance](../../../3d-applications/3ds-max/settings-1/substance-settings.md).

   ![](../../../assets/max6.png)

## Cambio de parámetros

1. Pulse dos veces en el nodo Substance para cargar los parámetros del Substance en la ventana de parámetros.
1. Cambie los parámetros para actualizar las texturas del Substance automáticamente.

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/max4?$png$&jpegSize=200&wid=1276){width="500px"}

## Previsualización de salida

Puede definir un canal específico para la miniatura del nodo Substance.

1. En el menú desplegable Previsualización de salida , elija el canal que desea utilizar para la miniatura del nodo.

   ![](../../../assets/max7.png)

## Substance de segmentación

Puede utilizar las propiedades Coordenadas para estructurar las texturas del Substance y definir Canales de mapa.

![](../../../assets/max10.png)

## Flujos de trabajo de OpenPBR

Hay dos flujos de trabajo de OpenPBR disponibles en la **lista de flujos de trabajo** en el **menú Substance**: **Substance del OpenPBR** y **Substance del OpenPBR V-Ray**. Estos flujos de trabajo están diseñados para usarse con archivos SBSAR creados mediante el modelo de material OpenPBR en Substance 3D Designer o Sampler (OpenPBR ha sido el modelo predeterminado desde Designer V16.0 y Sampler V6.0 y posteriores).

![](../../../assets/maya-max-v3-1/3ds-max-openpbr-node-preview.png)

### ¿Qué es el OpenPBR?

OpenPBR es un modelo de sombreado de materiales abierto y basado en la física desarrollado por Adobe y Autodesk y que ha contribuido a la Academy Software Foundation (ASWF). Proporciona una definición de material unificada y compatible con todos los procesadores. Para obtener más información, visite la [documentación del OpenPBR](https://experienceleague.adobe.com/es/docs/substance-3d/general-knowledge/openpbr/openpbr-overview).

### Cuándo utilizar un flujo de trabajo de OpenPBR

Utilice un flujo de trabajo de OpenPBR cuando el archivo SBSAR se haya creado mediante el modelo de material de OpenPBR en Substance 3D Designer o Substance 3D Sampler. Si el SBSAR se ha creado utilizando el modelo de material estándar de Adobe (ASM), utilice el flujo de trabajo heredado compatible con su procesador (Arnold, V-Ray o V-Ray 6).

>[!NOTE]
>
> Si aplica un flujo de trabajo de OpenPBR a un material de ASM o un flujo de trabajo estándar a un SBSAR de OpenPBR, el plugin solo conectará las salidas que sean comunes a ambos modelos de material. El resultado puede ser incompleto.

### Flujos de trabajo de OpenPBR disponibles

**OpenPBR**

Utiliza el nodo openPBRSurface de 3ds Max nativo. Compatible con Arnold y V-Ray. Este es el flujo de trabajo recomendado para la mayoría de los usuarios que trabajan con materiales de OpenPBR en 3ds Max.

**OpenPBR - V-Ray**

Utiliza el material V-Ray (VRayMtl) en modo OpenPBR. Recomendada para usuarios cuya canalización esté específicamente diseñada en torno a configuraciones de materiales V-Ray.

### Cómo aplicar un flujo de trabajo de OpenPBR

![](../../../assets/maya-max-v3-1/3dsmax-substance-to-openpbr.png)

1. Seleccione su archivo SBSAR (OpenPBR) usando el botón Cargar Substance.
1. En el menú superior, seleccione OpenPBR o OpenPBR - V-Ray.
1. Haga clic en Crear red para crear la red de sombreador en el Editor de material de pizarra.
1. El plugin conecta automáticamente las salidas SBSAR a las entradas correspondientes del nodo OpenPBR.
1. Asigne el material a la malla de la forma habitual.

![](../../../assets/maya-max-v3-1/3ds-max-openpbr-overview.png)
