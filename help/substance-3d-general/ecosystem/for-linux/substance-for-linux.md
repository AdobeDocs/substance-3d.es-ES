---
helpx_url: "https://helpx.adobe.com/substance-3d-general/ecosystem/substance-for-linux.html"
breadcrumb-title: ''
description: Obtenga información sobre cómo descargar, instalar y activar aplicaciones de Substance 3D en Linux mediante el portal de acceso de descarga de Adobe.
helpx_creative_field: ""
helpx_description: Substance 3D General
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance 3D para Linux (ADA)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 081136918fdf7f431ecee47e5ce64d8b5235bb1b
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 0%

---


# Guía de implementación

Después de adquirir Substance 3D para Linux® a través de su contrato Enterprise, los productos y licencias correspondientes se aprovisionan en el portal [Acceso de descarga de Adobe (ADA)](https://download-access.adobe.com/lws/downloads). Deberá descargar tanto las compilaciones de software como los archivos de clave de licencia de ADA para implementar el software correctamente.

## Descargar compilaciones de software y comprar licencias de archivos de claves:

Inicie sesión en [Adobe Download Access](https://download-access.adobe.com/lws/downloads). Encuentre las compilaciones de software y los archivos de clave de licencia:

1. Utilice la lista desplegable Cuenta para seleccionar la cuenta en la que compró Substance 3D Linux.

   ![](../../assets/ADA1.png)
1. Vaya a Descargas con el vínculo en el encabezado de página.

   ![](../../assets/ADA2.png)
1. Haga clic en Ver descargas en el producto correspondiente.

   ![](../../assets/ADA3.png)
1. ADA cargará la información de licencia asociada con este ID y la mostrará en la siguiente tabla.
1. Haga clic en &quot;Descargar&quot; en la línea &quot;Certificado digital&quot; para descargar el archivo .zip que contiene los archivos de clave de licencia.

   * El archivo zip contiene una clave de licencia por producto.
   * La clave de licencia activará el producto en cada uno de sus equipos con licencia.

   ![](../../assets/ADA4.png)
1. Haz clic en &quot;Substance 3D&quot; Sampler, Painter o Designer para mostrar las compilaciones de software de Substance 3D Painter, Substance 3D Designer e Substance 3D Sampler.
1. Haga clic en &quot;Descargar&quot; para descargar el archivo de instalación del producto que desea instalar.

   ![](../../assets/ADA5.png)
1. Aparecerá una notificación de &quot;Descargar software&quot;. Haz clic en &quot;aceptar&quot;

   ![](../../assets/ADA6.png)

## Instalación y activación

Para instalar el software:

1. Haga doble clic en el archivo EXE del producto para iniciar el asistente de instalación.
1. Siga los pasos de instalación para completar la instalación.

Existen dos opciones para activar el software: la activación local o la activación de red.

### Activación local

1. Descomprima la carpeta zip descargada de ADA.
1. Inicie el software que desee activar.
1. En el asistente de activación, seleccione &quot;Activar usando un archivo de clave de licencia&quot;.

   ![](../../assets/LinuxActivation3.png)
1. Haga clic en &quot;Examinar&quot; y señale la ubicación del archivo de clave de licencia correspondiente.
1. Haga clic en &quot;Siguiente&quot; para activar el software.

### Activación de red

1. Descomprima la carpeta zip descargada de ADA.
1. Coloque los archivos de clave de licencia descomprimidos en una red montada compartida.
1. En el equipo del usuario, configure una variable de entorno que apunte al archivo de clave de licencia, como se explica en estas páginas:

   * Substance 3D Painter - <https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/pipeline-and-integration/configuration/environment-variables>
   * Substance 3D Designer - <https://experienceleague.adobe.com/en/docs/substance-3d-designer/using/pipeline-and-project-configuration/environment-variables>
   * Substance 3D Sampler - <https://experienceleague.adobe.com/en/docs/substance-3d-sampler/using/pipeline-and-integrations/environment-variables>
