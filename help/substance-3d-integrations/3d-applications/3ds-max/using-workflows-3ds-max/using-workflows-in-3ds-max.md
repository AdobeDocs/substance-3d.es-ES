---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/3ds-max/using-workflows-in-3ds-max.html"
breadcrumb-title: ""
description: Utilice flujos de trabajo de renderizado en 3ds Max para crear automáticamente redes de sombreador para diferentes renderizadores a partir de materiales de Substance.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > Using Workflows in 3ds Max
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Uso de flujos de trabajo en 3ds Max
user-guide-description: ""
user-guide-title: ""
source-git-commit: 335f3107fb325bb769325bff8c150b3e8b7ff054
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%
---

# Uso de flujos de trabajo en 3ds Max

El plugin Substance en 3ds Max contiene flujos de trabajo para crear automáticamente una red de sombreador compatible con los procesadores. Los flujos de trabajo de procesamiento se encuentran en el menú Substance.

![](../../../assets/maya-max-v3-1/3dsmax-all-presets.png)

Para utilizar un flujo de trabajo, seleccione el nodo Substance en el editor de materiales y, a continuación, elija el flujo de trabajo en el menú Substance.

![](../../../assets/max-workflow.gif)

## Flujos de trabajo de OpenPBR

Hay dos flujos de trabajo de OpenPBR disponibles en la **lista de flujos de trabajo** en el **menú Substance**: **Substance del OpenPBR** y **Substance del OpenPBR V-Ray**. Estos flujos de trabajo están diseñados para usarse con archivos SBSAR creados mediante el modelo de material OpenPBR en Substance 3D Designer o Sampler (OpenPBR ha sido el modelo predeterminado desde Designer V16.0 y Sampler V6.0 y posteriores).

![](../../../assets/maya-max-v3-1/3ds-max-openpbr-node-preview.png)

### ¿Qué es el OpenPBR?

OpenPBR es un modelo de sombreado de materiales abierto y basado en la física desarrollado por Adobe y Autodesk y que ha contribuido a la Academy Software Foundation (ASWF). Proporciona una definición de material unificada y compatible con todos los procesadores. Para obtener más información, visite la [documentación del OpenPBR](https://experienceleague.adobe.com/en/docs/substance-3d/general-knowledge/openpbr/openpbr-overview).

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
