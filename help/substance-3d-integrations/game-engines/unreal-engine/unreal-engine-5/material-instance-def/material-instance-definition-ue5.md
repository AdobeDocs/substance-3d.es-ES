---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/material-instance-definition-ue5.html"
breadcrumb-title: ''
description: Crea definiciones de instancias de materiales con materiales de Substance en Unreal Engine 5 para optimizar el rendimiento de procesamiento de la GPU.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Material Instance Definition - UE5
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Definición de instancia de material - UE5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---


# Definición de instancia de material - UE5

Puede utilizar instancias de material UE5 con Substance. Esto ahorrará un gran paso en el proceso de procesamiento de la GPU al no cargar nuevo material en el proceso. Se puede crear un MID en tiempo de ejecución o en el editor. Con la versión 5.0.0, hemos añadido compatibilidad total con la creación de instancias de materiales.

## Creación de una instancia de material en el editor

1. Haga clic con el botón derecho en el material creado UE5 de Substance y elija &quot;Crear instancia de material&quot;. Esto crea un material de instancia UE5.

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/screen-shot-2022-03-31-at-6-07-08-pm?$png$&jpegSize=300&wid=1472)
1. Haga clic con el botón derecho en la fábrica de instancias de substance y elija &quot;Crear una instancia de gráfico&quot;. Esto creará una instancia del gráfico y otro material UE5. Elimine el material UE5 recién creado, ya que no se utilizará.

   ![](../../../../assets/screen-shot-2022-03-31-at-6-10-38-pm.png)
1. Haga doble clic en la instancia de material creada en el paso 1 y active los parámetros de textura para todos los mapas.
1. Establezca la textura en la nueva textura INST creada en el paso 2. Esto configurará la instancia de material para que utilice los mapas de salida de substance del gráfico instanciado.

   ![](../../../../assets/screen-shot-2022-03-31-at-6-13-18-pm.png)

Ahora tiene una instancia de material UE5 que utiliza un conjunto específico de texturas de sustancia. Se trata de una forma más optimizada de trabajar con varias sustancias en un proyecto UE5. Para aprender a crear un MID usando un modelo, por favor, compruebe esta página. [Modelo(UE5): Instancia de material dinámico](https://helpx.adobe.com/es/substance-3d/unlisted/documentation/integrations/blueprint-dynamic-material-instance-152535142.html)
