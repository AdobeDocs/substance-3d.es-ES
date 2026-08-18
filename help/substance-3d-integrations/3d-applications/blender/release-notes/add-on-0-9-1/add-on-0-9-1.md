---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/blender/release-notes/add-on-0-9-1.html"
breadcrumb-title: ''
description: Revise las notas de la versión 0.9.1 del complemento Blender para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Blender > Release Notes > Add-on 0.9.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Add-on 0.9.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---


# Add-on 0.9.1

**Notas de la versión del complemento 0.91+**

* Nota: *La versión del complemento 0.91+ no tiene compatibilidad con versiones anteriores del complemento.*
* Rearquitectura del código base interno para mejorar el rendimiento y la estabilidad del complemento
* Interfaz de usuario renovada para mejorar la experiencia de usuario general
* Se ha añadido la interfaz de usuario para permitir modificar el mosaico predeterminado.
* Se ha agregado la compatibilidad para actualizar texturas en ciclos de vista de procesamiento
* Se ha añadido un control de errores en la consola para notificar si no se ha podido cargar una sustancia
* Se ha actualizado el menú flotante con acciones rápidas

**Sección de preferencias: Agregado/actualizado:**

* Exportar parámetro de formato de imagen; cuando las imágenes generadas en Blender se utilizan como entradas de imagen para un material de Substance, este formato se utiliza para guardar la imagen en la carpeta Temporal.
* Ruta de biblioteca de Sbsar; especifica la carpeta que se abre de forma predeterminada cuando se utiliza el botón Cargar para buscar un archivo de substance.
* Ruta de exportación de textura predeterminada (carpeta temporal) que emula la ruta que utiliza Substance 3D Painter para controlar las exportaciones de archivos no guardados
* Ruta relativa de la textura igual que la anterior, con la opción de utilizar claves como $matName para crear subcarpetas
* Archivos sbsar ruta relativa a la creación de una subcarpeta que empaqueta los archivos sbsar utilizados en el archivo de mezcla al guardar el proyecto
* Posibilidad de definir dinámicamente diferentes redes de sombreadores en las preferencias : en la red de sombreadores, posibilidad de definir diferentes variables por sombreador en función de las necesidades de los sombreadores
* En la sección Salidas de la red de sombreadores, tiene la posibilidad de definir si una salida está activada de forma predeterminada
* Posibilidad de definir el espacio de color (esto admitirá los flujos de trabajo de película de aces, exr lineal y blender, no solo srgb)
* Selección predeterminada del formato de imagen y la profundidad de bits
* Una salida genérica para configurar los valores de los usos de salida no definidos en el sombreado, por ejemplo, si tiene otra salida que el sombreado no utiliza de forma predeterminada, por ejemplo, como una máscara.
* Un filtro para cambiar el tipo de salidas (1 Solo salidas activadas, 2 Todas las salidas que están en el sombreador y en el Substance, 3 Todas las salidas disponibles en el Substance)
* Compatibilidad con métodos abreviados personalizados (editados)

**Sección de paneles de Substance 3D: Agregado/actualizado:**

* Posibilidad de ajustar y bloquear el valor del parámetro de segmentación y resolución
* Interfaz de usuario preestablecida actualizada : El menú desplegable de tipo de sombreado para cambiar el tipo de gráfico que los usuarios desean tener
* Se ha cambiado el parámetro de entrada de imagen a la entrada de imagen estándar utilizada en Blender. Ahora puede utilizar imágenes de mezclador y no solo archivos
* Capacidad para trabajar en varias instancias de Blender en cualquier momento
* Compatibilidad con el resaltado automático de materiales en el panel Substance 3D cuando el material se selecciona en la ventana gráfica
