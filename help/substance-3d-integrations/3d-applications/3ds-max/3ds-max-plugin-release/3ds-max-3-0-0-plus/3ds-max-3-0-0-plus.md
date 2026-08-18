---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/3d-applications/3ds-max/3ds-max-plugin-release-notes/3ds-max-3-0-0-plus.html"
breadcrumb-title: ''
description: Revise las notas de la versión del plugin 3ds Max 3.0.0 y posteriores para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > 3ds Max Plugin Release Notes > 3ds Max 3.0.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3Ds Max 3.0.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# 3ds Max 3.0.0+

## 3ds Max 3.0.4

<b>Agregado/actualizado:</b>

* Iconos de plugins de Substance actualizados con los iconos más recientes.
* Se ha agregado la compatibilidad para enviar y recibir ajustes preestablecidos mediante Connector en el complemento.
* Administrador de Menús Integrado desde el parámetro de notificación para reemplazar el uso de la interfaz principal.

<b>Corregido:</b>

* Se ha resuelto un problema en el cual los materiales de Substance 2 podrían no procesarse en IR/Producción con Corona cuando el editor de materiales de pizarra está abierto y se selecciona el mapa de texturas de Substance2.
* Se ha resuelto el problema por el que las actualizaciones de Sampler Connector creaban nuevos nodos de Substance2 en lugar de actualizar los existentes.
* Se ha resuelto el problema de bloqueo en el plugin 3ds Max al añadir un nodo Substance2 y se ha garantizado que el uso de la importación por lotes para cargar archivos .sbsar ya no abra el editor de scripts.
* Se ha resuelto el problema por el que el plugin 3DSMax 2025 no se podía cargar debido a un archivo .dll incompatible al utilizar el instalador .msi.

## 3ds Max 3.0.2

<b>Agregado/actualizado:</b>

* Administración estandarizada de iconos en el plugin de Substance incorporando todos los iconos existentes en los archivos qrc y rcc, alineándose con los métodos preferidos de Autodesk y asegurando una carga consistente en el panel de gráficos SBSAR.
* Se ha mejorado la capacidad de respuesta de la ventana Configuración de Substance del complemento para garantizar que los campos de entrada y sus descripciones se ajusten correctamente al ajustar el tamaño de la ventana.
* El complemento Substance ahora es compatible con Corona 11.

<b>Corregido:</b>

* Se ha resuelto un problema por el que la rugosidad de Color de brillo y brillo no se conectaba automáticamente en los materiales de V-Ray. Ahora, ambas propiedades se vincularán automáticamente al crear un flujo de trabajo en V-Ray y Arnold.
* Se ha corregido un problema de la interfaz de usuario en el complemento por el que el ajuste del límite de núcleos de CPU mostraba incorrectamente valores de dos dígitos si el valor guardado era de un solo dígito.
* Se ha corregido un error de procesamiento en la consola del plugin 3ds Max v3.0.0 relacionado con la función de compatibilidad del Substance. Ahora, los nodos de substance creados mediante el menú Substance importación por lotes se procesan del modo esperado.
