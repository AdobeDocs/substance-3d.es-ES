---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/3ds-max/substance-in-3ds-max-overview.html"
breadcrumb-title: ''
description: Obtenga más información sobre el plugin Substance para 3ds Max y cómo importar y utilizar materiales de Substance en sus proyectos.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > Substance in 3ds Max Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Descripción general de Substance en 3ds Max
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---


# Descripción general de Substance en 3ds Max

## Descripción general del complemento:

## Abrir un Substance

1. Abra el Editor de pizarra, busque Substance y arrastre el nodo Substance2 a la vista.
1. Haga doble clic en el nodo Substance para activar las propiedades y, en Explorador de paquetes de Substance, cargue un Substance.

   >[!NOTE]
   >
   > También puede arrastrar y soltar el archivo .sbsar en el Editor de pizarra para crear automáticamente el nodo e importar la barra de pizarra.
1. Si un Substance contiene varias gráficas, puede elegir la gráfica que desea generar como material en el menú desplegable Gráfica seleccionada.

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/max8?$png$&jpegSize=100&wid=341)

   ![](../../../assets/max1.png)
1. Con el nodo Substance seleccionado, vaya al menú Substance y elija un procesador compatible. El material se creará y estará listo para aplicarse al objeto. Las texturas Substance se enlazan con el material de representación.

   | Renderizadores compatibles |
   | --- |
   | Arnold |
   | Variar |
   | Corona |
   | Octano |

   ![](../../../assets/max3.png)

## Cambio de resolución:

1. Establezca la resolución deseada para las texturas de Substance calculadas en los Ajustes de salida del Substance.
1. Para obtener una resolución de hasta 8 K, asegúrese de que está utilizando el motor de GPU, que se establece en [Configuración de Substance](../../../3d-applications/3ds-max/settings-1/substance-settings.md).

   ![](../../../assets/max6.png)

## Cambio de parámetros:

1. Pulse dos veces en el nodo Substance para cargar los parámetros del Substance en la ventana de parámetros.
1. Cambie los parámetros para actualizar las texturas del Substance automáticamente.

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/max4?$png$&jpegSize=200&wid=1276){width="500px"}

## Configuración de previsualización de salida:

Puede definir un canal específico para la miniatura del nodo Substance.

1. En el menú desplegable Previsualización de salida , elija el canal que desea utilizar para la miniatura del nodo.

   ![](../../../assets/max7.png)

## Substance de segmentación:

Puede utilizar las propiedades Coordenadas para estructurar en mosaico las texturas del Substance y definir Canales de mapa.

![](../../../assets/max10.png)
