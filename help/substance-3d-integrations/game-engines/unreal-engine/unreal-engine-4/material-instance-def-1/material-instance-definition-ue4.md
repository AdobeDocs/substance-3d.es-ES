---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/material-instance-definition-ue4.html"
breadcrumb-title: ''
description: Crea definiciones de instancias de materiales con materiales de Substance en Unreal Engine 4 para optimizar el rendimiento de procesamiento de la GPU.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Material Instance Definition - UE4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Definición de instancia de material - UE4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---


# Definición de instancia de material - UE4

Puede utilizar instancias de material UE4 con Substance. Esto ahorrará un gran paso en el proceso de procesamiento de la GPU al no cargar un nuevo material para procesar. Se puede crear un MID en tiempo de ejecución o en el editor. Con la versión 4.24.0.3, hemos añadido compatibilidad total con la creación de instancias de material e introducimos un nuevo flujo de trabajo de plantilla de material con salidas numéricas admitidas por el Substance Engine. Las plantillas de material permiten definir exactamente cómo desea configurar los sombreadores de material de Substance en UE4.

Al importar un archivo sbsar, puede elegir la plantilla con la que desea trabajar.

![](../../../../assets/ue4-material-templates.png)

Enviamos plantillas para trabajar con materiales de desplazamiento, refracción y alineados con el mundo que han incorporado controles para ajustar el azulejo, el tamaño de la textura, el desplazamiento y los parámetros de emisión. El sistema de plantillas de materiales también le permite proporcionar sus propias plantillas personalizadas.

![](../../../../assets/ue4-material-instance-params.png)

## Creación de una instancia de material en el editor

1. Haga clic con el botón derecho en el material creado UE4 de Substance y elija &quot;Crear instancia de material&quot;. De este modo, se crea un material con instancias UE4.

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/01-12?$png$&jpegSize=100&wid=592){width="560px"}
1. Haga clic con el botón derecho en la fábrica de instancias de substance y elija &quot;Crear una instancia de gráfico&quot;. Esto creará una instancia del gráfico y otro material UE4. Elimine el material UE4 recién creado, ya que no se utilizará.

   ![](../../../../assets/02-10.png){width="300px"}
1. Haga doble clic en la instancia de material creada en el paso 1 y active los parámetros de textura para todos los mapas.
1. Establezca la textura en la nueva textura INST creada en el paso 2. Esto configurará la instancia de material para que utilice los mapas de salida de substance del gráfico instanciado.

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/03-6?$png$&jpegSize=200&wid=1011){width="800px"}

Ahora tiene una instancia de material UE4 que utiliza un conjunto específico de texturas de sustancia. Se trata de una forma más optimizada de trabajar con varias sustancias en un proyecto UE4. Para aprender a crear un MID usando el modelo, por favor, compruebe esta página. [Modelo(UE4): Instancia de material dinámico](https://helpx.adobe.com/es/substance-3d/unlisted/documentation/integrations/blueprint-dynamic-material-instance-152535142.html)
