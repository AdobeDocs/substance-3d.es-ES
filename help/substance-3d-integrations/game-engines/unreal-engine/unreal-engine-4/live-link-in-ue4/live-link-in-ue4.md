---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/live-link-in-ue4.html"
breadcrumb-title: ''
description: Usa Live Link en Unreal Engine 4 para sincronizar materiales de Substance entre Painter y UE4 en tiempo real.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Live Link in UE4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Live Link en UE4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---


# Live Link en UE4

>[!WARNING]
>
> Live Link en Unreal Engine ya no es compatible. Los usuarios con una versión anterior del plugin donde se utiliza Live Link podrán seguir utilizando la función.

>[!WARNING]
>
> Live Link no funciona con mallas BSP UE4. El recurso que envíe debe ser un archivo de modelo importado en su proyecto UE4

## Establecimiento del vínculo con el Substance Painter

1. Abrir Substance Painter
1. Haz clic con el botón derecho en el contenido que deseas enviar a Painter en el Navegador de contenido y elige &quot;Enviar a Painter&quot;.

   ![](../../../../assets/link1-22.png){width="400px"}
1. La malla aparecerá en Substance Painter y podrá comenzar a aplicar texturas. A medida que trabaje, las texturas se enviarán a UE4 y se aplicarán a los materiales. El punto verde del icono UE4 de la barra de herramientas indica que el vínculo está activo y envía texturas.

   ![](../../../../assets/icon-12.png)

   1. Puede pausar la transmisión de datos en las opciones de configuración del complemento. Vaya a Complementos>dcc-live-link y elija Configurar. Desactive la opción Activar streaming para detener el envío de datos a UE4.

      ![](https://helpx-prod.scene7.com/is/image/HelpxProd/config-6?$png$&jpegSize=100&wid=393)
1. Las texturas de Painter aparecerán en el navegador de contenido y se aplicarán al material en UE4.

   ![](../../../../assets/link3-11.png){width="500px"}
1. Se creará un proyecto de Substance Painter (.spp) en la carpeta del proyecto UE4 en una carpeta denominada &quot;.sp&quot;

   ![](../../../../assets/link4-5.png)

## Restablecimiento de un vínculo con el Substance Painter

Puede continuar donde lo dejó después de cerrar Painter o Unity.

1. Abra el proyecto .spp en el Substance Painter ubicado en la carpeta Unity project>assets>.sp.
1. Haga clic con el botón derecho en la malla del navegador de contenido y elija &quot;Enviar a Painter&quot; para restablecer el vínculo.

   ![](../../../../assets/link5-3.png){width="600px"}
