---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/3d-applications/maya/maya-plugin-release-notes/maya-3-0-0-plus.html"
breadcrumb-title: ''
description: Revise las notas de la versión 3.0.0 y posteriores del plugin Maya para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > 3ds Max Plugin Release Notes > Maya 3.0.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maya 3.0.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Maya 3.0.0+

## Maya 3.0.3

<b>Agregado/actualizado:</b>

* Sistema de almacenamiento en caché del complemento Maya mejorado para almacenar en caché solo una vez tras la creación inicial de la red, con el almacenamiento en caché manual habilitado.
* Se proporcionó una opción para cambiar la ubicación de la carpeta &quot;substance&quot; en el complemento Maya.
* Se ha actualizado el sistema de importación de flujo de trabajo del plugin Maya para garantizar la compatibilidad con la actualización de Autodesk a Python 3.12.
* Iconos de plugins de Substance actualizados con los iconos más recientes.
* Se ha agregado la compatibilidad para enviar y recibir ajustes preestablecidos mediante Connector en el complemento.

<b>Corregido:</b>

* Se ha solucionado el problema por el que al cargar o descargar el plugin de Substance para Maya se producía una pantalla de error y se bloqueaba.
* Se han solucionado problemas de almacenamiento en caché, garantizando específicamente que los archivos .exr hagan referencia correctamente, y reduciendo los bloqueos relacionados con el almacenamiento en caché en escenas grandes.
* Se ha resuelto el problema por el que la vista previa del material en la ventana de muestra no se mostraba cuando se cargaba un archivo SBSAR en el plugin Maya.
* Se ha resuelto el problema por el que Connector no recibía el archivo SBSAR si al menos un SBSAR ya estaba en Hypershade.
