---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/3d-applications/maya/substance-in-maya-overview.html"
breadcrumb-title: ""
description: Obtenga información sobre el complemento Substance para Maya y cómo importar y utilizar materiales de Substance en su flujo de trabajo.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Substance in Maya Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance en Maya Resumen
user-guide-description: ""
user-guide-title: ""
source-git-commit: 28a9d8cf7a4eed4163f99e8158c9cb8f9da88302
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%
---

# Substance en Maya Resumen

## Descripción del complemento

El complemento Substance para Maya le permite cargar cualquier material de Substance 3D existente (archivo .SBSAR) directamente en Maya. Los materiales de Substance 3D se pueden crear y exportar como archivos SBSAR desde Substance 3D Designer o Substance 3D Sampler, y descargar desde bibliotecas existentes como la biblioteca de Substance 3D Assets. El plug-in Substance para Maya crea materiales Maya e introduce las texturas de salida en las entradas correctas del canal de materiales

>[!NOTE]
>
> Asegúrese de tener el plugin cargado en Configuración/Preferencias ->Administrador de plugins Maya

## Abrir un archivo SBSAR en el Editor de nodos de hipersombreado

1. Abra **Hypershade** y en el **Editor de nodos**, haga clic con el botón derecho y deslícese hacia arriba en el menú de marcado para elegir **Crear nodo**. Desde la **ventana Crear nodo**, busque y seleccione el **nodo Substance**.

   ![](../../../assets/createnode.png)

   Haga clic en el **nodo Substance** en el hipersombreado para seleccionarlo. Se abrirá el **Editor de materiales**, donde puedes cargar tu material de Substance 3D (archivo SBSAR) haciendo clic en el icono de carpeta.

1. También puedes arrastrar y soltar un archivo SBSAR en el **Editor de Hipersombras** de Maya, y hacer clic en el nodo de Substance creado automáticamente para ver y editar directamente las opciones en el **Editor de Materiales**.

### Jugar con parámetros SBSAR en el Editor de propiedades

![](../../../assets/1.png)

1. La lista desplegable **Gráfico seleccionado** se rellena si el Substance contiene varios gráficos. Seleccione el gráfico que desea utilizar para crear el material.

1. El botón **Información de gráfico** muestra los atributos de gráfico establecidos en Substance Designer.

1. Establezca la Resolución estableciendo los valores **Ancho** y **Height**. Deshabilite **Bloquear proporción** para elegir proporciones no cuadradas.

1. Habilite **Almacenar en caché salidas en disco** para hacer un bake las salidas de Substance en disco para que se puedan usar con procesadores como Arnold. El complemento volverá a leer el archivo en caché mediante un nodo de archivo Maya.

   ![](../../../assets/outputsettings.png)

1. Elija un flujo de trabajo para el procesador que esté utilizando y haga clic en el botón **Crear red de Sombreador**. Se crea una red de sombreador para el flujo de trabajo del procesador. Para las versiones 3.1.1., la lista de flujos de trabajo también ofrece la opción de crear redes de sombreador de OpenPBR. Una vez creada la red de sombreador, puede aplicar el material en la escena.

   ![](../../../assets/createnetwork.gif){width="1000px"}

## Resolución de problemas

Para informar de un error, únete al canal #maya-plugin en el [servidor Substance Discord](https://discord.com/invite/substance3d) o visita las [comunidades de Adobes](https://community.adobe.com/t5/substance-3d-plugins/ct-p/ct-substance-3d-plugins?page=1&sort=latest_replies&lang=all&tabid=all&topics=label-autodesk3dsmax). La inclusión de información relevante del registro de la consola y cualquier paso de reproducción nos ayudará a diagnosticar el problema de manera más eficiente.