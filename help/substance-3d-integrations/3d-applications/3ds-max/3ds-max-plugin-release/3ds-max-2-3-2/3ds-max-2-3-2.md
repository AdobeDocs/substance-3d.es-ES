---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/3d-applications/3ds-max/3ds-max-plugin-release-notes/3ds-max-2-3-2.html"
breadcrumb-title: ''
description: Revise las notas de la versión 2.3.2 del plugin 3ds Max para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > 3ds Max Plugin Release Notes > 3ds Max 2.3.2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3ds Max 2.3.2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---


# 3ds Max 2.3.2

Publicado el 8 de abril de 2020

Hoy hemos lanzado la versión 2.3.2 del plugin, que es principalmente una versión de corrección de errores en la parte superior de 2.3.1.

2.3.2 Versión:

* Substance Engine actualizados a 7.2.9
* Se ha solucionado un problema con el procesamiento por el cual Redshift/VRay se bloqueaba en 3ds Max en 2018, 2019 y 2020
* Los errores de aserción de depuración ya no aparecerán
* El nodo Substance2 ahora tiene correctamente las interfaces de secuencias de comandos para iMultipleOutputChannelsWithValues
* La entrada Origen del Substance en el menú ahora abrirá el Iniciador del Substance a la pestaña Origen si está instalado
* Los materiales de Substance ahora deben actualizarse correctamente al trabajar con el procesador de Corona
* Las salidas de Substance ya no se sustituyen temporalmente por imágenes cuando se utilizan con VRay Next
* El cuadro de diálogo de compatibilidad de procesamiento no aparece automáticamente. Sigue estando disponible en el cuadro de diálogo de configuración si es necesario
* Se ha corregido un posible problema con la exportación de un fbx mientras el material de Substance se aplicaba en 3ds Max 2021

Problemas conocidos:

* En 3ds Max 2018, la exportación de un fbx con un material de Substance adjunto al objeto se bloquea en el plugin fbxmax.dlu. Actualmente estamos hablando con Autodesk para ver si hay algo en nuestro extremo que se pueda hacer o si es una limitación de la versión anterior de la integración fbx. La solución alternativa anterior no era fiable y se eliminó. Esto no ocurre en 3ds Max 2019 o posterior.

Esta versión está disponible para 3ds Max 2018, 2019, 2020 y 2021.
