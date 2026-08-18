---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/modo/substance-in-modo-overview.html"
breadcrumb-title: ''
description: Obtenga más información sobre el plugin Substance para MODO y cómo importar y utilizar materiales de Substance en el flujo de trabajo.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Substance in MODO Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Descripción general de Substance en MODO
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 5%

---


# Descripción general de Substance en MODO

## Descripción general:

## Abrir un Substance

1. Cree un material o seleccione un grupo de materiales.
1. En Textura > Substance, elija crear Substance o utilice el botón Crear en las opciones del kit de Substance. Esto creará un material Substance en el árbol del sombreador.
1. Haga clic en la barra de carga para cargar un archivo sbsar.

   ![](../../../assets/load-1.png)

## Creación de salidas

Con el **Modo de Sombreado predeterminado - de principio**, puede crear salidas mediante el flujo de trabajo de metal/rugosidad.

1. En la sección Salidas de las propiedades del Substance, haga clic en los resultados necesarios para el sombreado. Se generará la textura del Substance, que se añadirá al árbol del sombreador con el efecto de capa de material correcto. Para el modo de Sombreado de principio, necesitará lo siguiente:

   | Salida de Substance | Espacio de color | Efecto de capa de material (modo de Sombreado de principios) |
   | --- | --- | --- |
   | Color base | sRGB | Color difuso |
   | Normal | Lineal | Normal |
   | Rugosidad | Lineal | Rugosidad |
   | Metálico | Lineal | Metálico |

   ![](../../../assets/outputs-3.png)

## Cambio de Resolución/Parámetros

Puede cambiar los parámetros del Substance para actualizar o cambiar las texturas generadas. Si se cambia un parámetro, el Substance Engine volverá a calcular las texturas que se introducen en el material MODO.

1. Vaya a Propiedades del Substance para el material del Substance y, en la sección Ajustes, cambie cualquiera de los parámetros.

   ![](../../../assets/params.png)
1. Puede cambiar la resolución de las texturas generadas mediante el menú desplegable Tamaño de salida . Los Substance se pueden configurar para que generen hasta 8 000. Se requiere el [motor de GPU Substance](../../../3d-applications/modo/modo-switch-engine/modo-switch-engine.md) para la salida de 8K.
