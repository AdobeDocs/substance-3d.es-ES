---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/blender/release-notes/blender-add-on-2-0-0.html"
breadcrumb-title: ''
description: Revise las notas de la versión 2.0.0 del complemento Blender para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Substance 3D Integrations
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Add-on 2.0.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---


# Add-on 2.0.0

El Substance 3D Addon 2.0 marca una actualización transformativa para los usuarios de Blender, con una arquitectura de plugin completamente refactorizada. Este rediseño se centra en una integración perfecta, un rendimiento mejorado y una base flexible para futuras expansiones. No se trata solo de una actualización, sino de una reconcepción de la forma en que se gestionan los materiales Substance en Blender, para satisfacer las necesidades en constante evolución de los profesionales del diseño 3D.

<b>Aspectos destacados de la versión 2.0:</b>

* Arquitectura refactorizada: estructura de plugins mejorada para mejorar el rendimiento y la integración
* Compatibilidad con futuras ampliaciones: la actualización sienta las bases para añadir fácilmente nuevas funciones en el futuro
* Compatibilidad más amplia: totalmente compatible con las versiones 3.0 y superiores de Blender, incluida la compatibilidad con usuarios de Mac.

<b>Agregado/actualizado:</b>

* [SRE] Compatibilidad con la selección de Substance Engine (la GPU es la predeterminada)
* [SRE] Nuevos formatos de imagen para exportar las texturas
* [SRE] Selección de Profundidades de bits para cada tipo de mapa
* [BLD] Compatibilidad con salidas de valor
* [BLD] Compatibilidad con la entrada de cadenas
* [SRE] Se ha añadido la opción de seleccionar la carpeta temporal predeterminada para el destino de exportación de la imagen

<b>Corregido:</b>

* [SRE] Mejora global del rendimiento
* [BLD] Se han solucionado problemas de comunicación entre las herramientas de integración y Blender
* [BLD] Las herramientas de integración no se pueden instalar o iniciar
* [BLD] Las herramientas de integración no finalizan al cerrar Blender
* [BLD] El material no se actualiza al cambiar el tipo de archivo de un mapa
* [SRE] Todos los mapas de los materiales se exportan todo el tiempo
* [SRE] Las herramientas de integración exportan mapas normales con escalones
* [SRE] La carga del Substance nunca termina
* [SRE] Las unidades de Tamaño físico no se ajustan a la escena
* [BLD] Los ajustes preestablecidos generados en Blender no funcionan con otras integraciones
* [BLD] El material no se actualiza en Ciclos
* [BLD] Se ignoran los límites blandos y duros de las entradas
* [BLD] La intensidad de color no se actualiza correctamente al ajustar un parámetro
* [SRE] La desinstalación de las herramientas de integración falla
* [SRE] Se ha solucionado el problema por el que la duplicación de materiales varias veces provocaba un error.
* [SRE] El espacio de color de los nodos de imagen ahora coincide correctamente con las preferencias del usuario.

<b>Problemas conocidos:</b>

* Al utilizar Blender v4.0+, los sockets no están en orden después de activar y desactivar varias veces
* Cltr+Z para deshacer los cambios puede causar errores
* Cargar un archivo vacío o una carpeta en lugar de un archivo .sbsar podría romper el complemento
* Compatibilidad con el modo sin cabeza de Blender
