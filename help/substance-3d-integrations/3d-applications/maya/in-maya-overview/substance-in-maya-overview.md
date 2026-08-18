---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/maya/substance-in-maya-overview.html"
breadcrumb-title: ''
description: Obtenga información sobre el complemento Substance para Maya y cómo importar y utilizar materiales de Substance en su flujo de trabajo.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Substance in Maya Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance en Maya Resumen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# Substance en Maya Resumen

## Descripción del complemento

El plugin Substance le permite cargar un material Substance creado en Substance Designer directamente en Maya. El plugin creará un material maya y alimentará las texturas de la sustancia en los canales de materiales de entrada. A continuación, puedes realizar cambios en los parámetros de substance y las texturas se actualizarán automáticamente.

>[!NOTE]
>
> Asegúrese de tener el plugin cargado en Configuración/Preferencias ->Administrador de plugins Maya

![](https://helpx-prod.scene7.com/is/image/HelpxProd/plugin-4?$png$&jpegSize=100&wid=618)

## Abrir un Substance

1. Abra el Hipersombreado y, en el Editor de nodos, haga clic con el botón derecho y deslice el dedo hacia arriba en el menú de marcado para elegir Crear nodo. Se abrirá la ventana Crear nodo. Desde allí, puede buscar el nodo Substance.

   ![](../../../assets/createnode.png)

   También puede pulsar la tecla Tab en el editor de nodos y, en el campo de texto, escribir substance ; esta acción se filtrará a las opciones de substance . En las opciones, elija Textura de Substance.
1. Seleccione el nodo Substance y, en el Editor de propiedades, busque y cargue un archivo de Substance (.sbsar).

   ![](../../../assets/1.png)
1. La lista desplegable Gráfico seleccionado se rellenará si el Substance contiene varios gráficos. El gráfico elegido se utilizará para crear el material.
1. El botón Información de gráfica mostrará los atributos de gráfica definidos en Substance Designer.
1. Establezca la Resolución eligiendo un valor en el cuadro desplegable Anchura y Height. Bloquear relación está activado de forma predeterminada.
1. Habilite Almacenar en caché salidas en disco para convertir las salidas de Substance en disco de modo que se puedan utilizar con procesadores como Arnold. El complemento volverá a leer el archivo en caché mediante un nodo de archivo Maya.

   ![](../../../assets/outputsettings.png)
1. Elija un flujo de trabajo para el procesador que esté utilizando y haga clic en el botón Crear red de sombreadores. Se crea una red de sombreadores para el flujo de trabajo del procesador. Ahora puede aplicar el material en la escena.

   ![](../../../assets/createnetwork.gif){width="1000px"}
