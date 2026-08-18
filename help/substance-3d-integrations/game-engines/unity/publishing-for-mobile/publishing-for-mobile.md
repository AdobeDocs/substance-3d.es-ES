---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/publishing-for-mobile.html"
breadcrumb-title: ''
description: Optimiza los materiales de Substance para las plataformas móviles en Unity ajustando la configuración y las resoluciones de textura.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Publishing for Mobile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Publicación para dispositivos móviles
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# Publicación para dispositivos móviles

>[!NOTE]
>
> **Tamaño de textura en dispositivos móviles**
> 
> La resolución de la textura establecida en el Editor de Unity será del tamaño que se publique en el binario de la aplicación. Reducir la resolución del material Substance creará texturas con tamaños de archivo más pequeños.

## Plataformas

## Apple iOS

1. Asegúrese de que el módulo iOS se haya descargado para la versión de Unity correspondiente.
1. En Unity, cambie el destino de compilación a iOS.
1. Abra la configuración del reproductor y cambie el campo &quot;Identificación - Identificador de paquete&quot; por otro más exclusivo. (por ejemplo: com.Adobe.ios (Project)
1. Crea y ejecuta el juego.
1. En Xcode, haga clic en el dispositivo iOS y cambie el menú desplegable &quot;Firma - Equipo&quot; por su ID de equipo de desarrolladores.
1. En el dispositivo iOS, vaya a &quot;Configuración - General - Administración de dispositivos&quot; y haga clic en &quot;Confiar&quot; en el ID del equipo de desarrolladores que aparece.
1. Ejecute de nuevo la compilación de Xcode haciendo clic en el botón &#39;Generar y ejecutar el esquema actual&#39; (el botón Reproducir).
1. El juego debe estar ejecutándose en el dispositivo iOS.

## Sistema operativo Android

1. Asegúrese de que el módulo Android se haya descargado para la versión de Unity correspondiente.
1. En Unity, cambie el destino de compilación a Android.
1. Abra la configuración del reproductor y cambie el campo &quot;Identificación - Identificador de paquete&quot; por otro más exclusivo. (por ejemplo: com.Adobe.android (Project)
1. Crea y ejecuta el juego.
1. El juego debe ejecutarse en el dispositivo Android.
