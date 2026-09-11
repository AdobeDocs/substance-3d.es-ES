---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/installing-to-source-builds-ue5.html"
breadcrumb-title: ''
description: Instale el complemento de Substance 3D en las compilaciones de origen de Unreal Engine 5 para realizar modificaciones personalizadas del motor.
helpx_creative_field: ""
helpx_description: Substance 3D Integrations
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Instalación en versiones de origen - UE5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---


# Instalación en versiones de origen - UE5

El plugin de Substance se puede usar con versiones de Unreal Engine creadas a partir de la fuente. Para ello, el complemento se puede instalar en una carpeta de proyecto de C++ o en la carpeta del motor de una generación de código fuente.

>[!NOTE]
>
> Estos métodos requieren que tenga una versión del complemento descargada de la tienda. La carpeta del plugin del Substance se puede transferir entre equipos y compilaciones UE.

## Instalar en una carpeta de proyecto de C++

1. En la carpeta del proyecto, cree una carpeta Complementos si todavía no existe.
1. Dentro de la carpeta Plugins, cree una carpeta de tiempo de ejecución.
1. Coloque la carpeta Substance dentro de la carpeta Runtime. USUARIOS DE LINUX: Después del paso 3, busque la carpeta &quot;include&quot; en la carpeta del Substance y cámbiele el nombre para poner en mayúscula la &quot;i&quot; (include > Include).
1. Inicie Unreal Engine.
1. Abra el proyecto de C++ mediante el iniciador.
1. Después de iniciar el proyecto, Unreal Engine le preguntará si desea reconstruir los componentes del plugin antes de iniciar, seleccione Sí. Esto se hará mediante Microsoft Visual Studio (Windows, Linux) o Xcode (Mac).
1. Unreal Engine se cerrará, pero los componentes se generarán en segundo plano. Este proceso puede tardar unos 5 minutos. Una vez hecho esto, el proyecto se abrirá. Si falla, aparecerá una ventana de error.

## Instalación en la carpeta del motor

>[!NOTE]
>
> Se deben seguir los pasos anteriores para volver a generar la carpeta de archivos binarios del complemento antes de poder instalar el complemento en la carpeta Engine.

1. Copie la carpeta del Substance desde dentro de la Carpeta del proyecto > Complementos > Tiempo de ejecución.
1. Abra la carpeta de la versión de Unreal Engine y vaya a Motor > Complementos > Marketplace.
1. Pegue la carpeta Substance.
1. Abra el Editor de Unreal Engine. Cree un nuevo proyecto si lo desea.
1. Abra el menú Complementos y compruebe que el complemento Substance está activado.
