---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/3d-applications/maya/maya-plugin-release-notes/maya-2-1-0.html"
breadcrumb-title: ''
description: Revise las notas de la versión 2.1.0 del plugin Maya para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Maya Plugin Release Notes > Maya 2.1.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maya 2.1.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---


# Maya 2.1.0

Substance en Maya 2.1.0 changelog

* Compatibilidad garantizada con Python 3
* Substance Engine actualizados a la versión 7.2.9
* Se ha corregido un error con nombres de variable de menú global en conflicto al aplicar un flujo de trabajo
* El flujo de trabajo de Redshift ahora establece fresnel en metalness
* Se ha añadido un nuevo archivo de plugin, substancelink, que gestiona la interoperabilidad con otros programas de Substance y el Iniciador de Substance
* Al abrir Substance Source ahora, se abrirá el Iniciador de Substance en la pestaña Origen si se ha cargado el plugin substance.link
* El plugin substanceLink permite al Launcher, cuando se añade la interfaz de usuario, enviar materiales del Substance Source a la integración Maya
* Comandos de scripts añadidos para obtener versiones de bibliotecas internas, así como para abrir el iniciador de sustancias en la página de origen
* Los vínculos a sitios web ahora se abren en [substance3d.com](http://substance3d.com) en lugar de en [allegorithmic.com](http://allegorithmic.com)
* Al abrir una página web, los vínculos de documentación y de origen ahora abren el explorador predeterminado definido por el usuario
* En Windows, Internet Explorer ya no está abierto
* Se ha añadido un nuevo vínculo en el estante y el menú del Substance share
* Se han añadido nuevos comandos para consultar la versión y el hash de Substance Linker
* En Maya LT, la versión se ha eliminado del menú de configuración
* El menú Acerca de ya no se escribe en PySide2 y Python, sino en código nativo mediante Qt. Ahora está disponible en Maya LT, donde antes no lo estaba.
* El menú Acerca de tiene información de diagnóstico diferente; ahora muestra el hash git para que coincida con el cambio en el control de código fuente
* La copia del menú Acerca al portapapeles ahora también tendrá este hash git, junto con la versión de Maya para la que está construido el plugin.
* Las licencias de la ventana Acerca de ahora se abren como un archivo de texto
* Se ha agregado la compatibilidad con Maya 2017
* El generador de secuencias de comandos de flujo de trabajo ya no genera cadenas para el miembro &#39;order&#39;. Cualquier flujo de trabajo existente se gestionará correctamente

Comandos de scripts añadidos:\
substanciemaya:\
\* substanceUtilityGetLinkerVersion\
\* substanceUtilityGetLinkerHash\
\* substanceUiOpenAboutWindow\
\* substanceUiOpenSourceWebsite\
\* substanceUiOpenDocumentation\
\* substanceUiOpenShareWebsite

substance.link:\
\* substanceLinkGetLinkVersion\
\* substanceLinkGetPortalCliVersion\
\* substanceLinkOpenLauncher

Esta versión está disponible para Maya 2017, 2018, 2019 y 2020 en Windows,\
Linux y Macos. También se lanza para Maya LT 2018, 2019 y 2020 en\
Windows y MacOS.
