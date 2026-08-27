---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/material-template-usage-ue5/out-of-the-box-material-templates.html"
breadcrumb-title: ''
description: Usa plantillas de materiales prediseñadas al importar materiales SBSAR a Unreal Engine 5 para una configuración y flujos de trabajo rápidos.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Material Template Usage - UE5 > Out-of-the-Box Material Templates
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Plantillas de material listas para usar
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---


# Plantillas de material listas para usar

Al importar materiales SBSAR en el navegador de contenido, puede elegir las diferentes plantillas de materiales en el menú desplegable que están disponibles de forma inmediata.

![](../../../../../assets/screen-shot-2022-05-10-at-8-58-45-pm-copy.png)

## Plantilla estándar de Substance

Esta es una plantilla de material básico para una experiencia UV genérica. Proporciona algunos controles básicos de las cantidades de UV para que pueda escalar los UV y estirar las texturas. Puede dividir la escala UV activando la opción Dividir UV; también tiene la cantidad U, la cantidad V, el Desplazamiento de UV y un ángulo de rotación UV. Esto le permite hacer algunas baldosas UV, así como la rotación UV.

![](../../../../../assets/screen-shot-2022-05-10-at-9-06-40-pm-copy.png)

## Plantilla triplanar de Substance

La plantilla triplanar realiza una asignación triplanar de los ángulos o caras X, Y y Z de la malla, de modo que combina tres proyecciones diferentes de las texturas para fusionar perfectamente los ángulos. La plantilla triplanar permite que los materiales se fusionen en las distintas caras a medida que el objeto se dobla

![menú de detalles de un material triplanar de Substance](../../../../../assets/triplanar-template.png)

La plantilla triplanar es compatible con el tamaño físico, por lo que, cuando se activa el tamaño físico, la plantilla triplanar escala las imágenes en función del tamaño físico del material, de modo que, independientemente de cuánto escale el objeto, la textura siempre seguirá siendo la misma y tendrá un aspecto uniforme. Obtenga más información sobre Tamaño físico aquí: [Tamaño físico - UE5](../../../../../game-engines/unreal-engine/unreal-engine-5/physical-size-ue5/physical-size-ue5.md)

## Plantilla de refracción de Substance

La plantilla de refracción se utiliza principalmente para objetos transparentes, por ejemplo, gafas. Permite modificar el valor IOR o las texturas estándar que se tendrían para un material de vidrio o un material transparente.

![](../../../../../assets/screen-shot-2022-05-10-at-9-07-38-pm.png)

## Substance Car Paint Template

La plantilla de pintura de coche añade un soporte de capa transparente e incluye soporte para los valores y las baldosas UV ajustables, valores de rugosidad de capa clara y valores de potencia de fresnel.

![menú de detalles de un material de Substance Car Paint](../../../../../assets/car-paint-template.png)

## Configuración de plantillas de Desplazamiento

>[!IMPORTANT]
>
> Plantillas experimentales
> 
> Advertencia: Las siguientes plantillas son experimentales y están sujetas a cambios importantes entre versiones. Estas plantillas hacen uso de la característica de nanita de Epic, que es a su vez experimental en el momento de este escrito. Es posible que no sean 100% estables y se debe tener precaución al utilizarlos en proyectos.

Siga estos pasos para habilitar completamente la compatibilidad con el desplazamiento de nanite en sus proyectos y utilizar materiales de desplazamiento con sus mallas.

1. Vaya a Carpeta del proyecto > Configuración > DefaultEngine.ini y ábralo
1. Añada lo siguiente a la sección [/Script/Engine.RendererSettings]:
   * r.Nanite.AllowTessellation=1
   * r.Nanite.Tessellation=1
1. Seleccione la malla estática a la que desea aplicar una plantilla de desplazamiento y abra su configuración.
1. Active la opción Habilitar compatibilidad con Nanite .
1. Importe el archivo .sbsar deseado en el navegador de contenido y seleccione el Substance\_Desplazamiento\_Plantilla o la carpeta Susbtance\_Triplanar\_Displacement\_Template
1. Para cambiar la cantidad de desplazamiento, vaya a la plantilla de material y seleccione el nodo de salida. A continuación, ajuste la Magnitud en la sección Desplazamiento.

## Plantilla de Desplazamiento de Substance

De forma similar a la plantilla estándar del Substance, esta plantilla permite el ajuste de los valores U y V al tiempo que añade compatibilidad con el Desplazamiento de nanita.

![menú de detalles de un material de Desplazamiento de Substance](../../../../../assets/displacement-template.png)

## Plantilla de Desplazamiento triplanar de Substance

De forma similar a la plantilla de Desplazamiento del Substance, esta plantilla aplica la proyección triplanar con la opción de compatibilidad con el Tamaño físico y la adición de compatibilidad con el Desplazamiento nanita.

![menú de detalles de un material de Desplazamiento triplanar de Substance](../../../../../assets/triplanar-displacement-template.png)
