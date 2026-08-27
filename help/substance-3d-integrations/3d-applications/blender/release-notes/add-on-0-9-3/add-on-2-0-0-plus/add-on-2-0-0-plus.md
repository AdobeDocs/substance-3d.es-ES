---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/3d-applications/blender/release-notes/add-on-0-9-3/add-on-2-0-0-plus.html"
breadcrumb-title: ''
description: Revise las notas de la versión del complemento Blender 2.0.0 y posteriores para obtener más información sobre las nuevas funciones y mejoras.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Blender > Release Notes > Add-on 2.0.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Add-on 2.0.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---


# Add-on 2.0.0+

## Complemento 2.2

<b>Agregado:</b>

* Compatibilidad con el procesador de octanos
* Compatibilidad inicial con Redshift
* Compatibilidad inicial con Renderman

<b>Actualizado:</b>

* Actualizado a la versión más reciente de Connector
* Se ha añadido la funcionalidad de recibir ajustes preestablecidos mediante el conector
* Se ha mejorado la funcionalidad de importación de ajustes preestablecidos: ahora, todas las instancias de un SBSAR que incluyan el material añadirán el ajuste preestablecido
* Funcionalidad del conector estandarizado

<b>Corregido:</b>

* Error de persistencia por el que la imagen de entrada no funcionaba después de guardar el archivo de mezcla
* Problema con la red de sombreado que no funciona al actualizar el ajuste preestablecido de sombreado
* URL incorrecta en el botón del plugin de descarga
* Mosaico invertido en octanos
* Valores de entrada que no funcionan con procesadores de terceros
* Problema en el que no se creó el parámetro de valor de entrada flotante
* Los espacios de color de Renderman no funcionan correctamente
* Los ajustes preestablecidos de sombreado no filtran por procesador disponible

## Complemento 2.1.1

Esta actualización incluye compatibilidad con Blender 4.0+ y varias funciones nuevas en las preferencias del complemento. También hemos agregado la compatibilidad con Substance Connector para la transferencia fluida de datos entre Substance 3D Sampler y Blender (Enviar a) y hemos solucionado algunos errores. Encuentra las notas de la versión detalladas a continuación.

<b>Agregado/actualizado:</b>

* Se ha añadido la funcionalidad de Substance Connector (admite archivos SBSAR y archivos USD).
* Compatibilidad con Blender 4.0+.
* Compatibilidad con SRE versión 2.1.0.
* En Preferencias Del Complemento:
  * Posibilidad de elegir la ruta de instalación de las herramientas de integración de Substance.
  * Botón para restablecer las herramientas de integración a la ruta predeterminada.
  * Botón para abrir la carpeta Herramientas de integración.
  * Se ha añadido Aplicar tipo para asignar material (Insertar: establézcalo como material principal, Anexar: agréguelo al final de la lista).
  * Se ha añadido una casilla de verificación para seleccionar el comportamiento predeterminado de los grupos de entrada (contraído/expandido).
  * Se ha añadido una casilla de verificación para seleccionar el comportamiento predeterminado de la única propiedad de actualización de texturas.
  * Inicie automáticamente el Substance Remote Engine al abrir Blender (importante habilitarlo si usa Connector).
* En el complemento:
  * Solo texturas de actualización agregadas (permite cambiar los parámetros sin rehacer el gráfico de nodos).
  * Se han añadido botones para expandir todos los grupos y contraer todos los grupos.
  * Se ha añadido el grupo de imágenes de entrada para agrupar todas las imágenes de entrada si es necesario en un SBSAR.
  * Las entradas de parámetros ahora se muestran en el mismo orden que Designer.
  * Se ha añadido una vista previa en miniatura de cada material de Substance.

<b>Corregido:</b>

* Se ha corregido el error del grupo de entrada General vacío.

<b>Problemas conocidos:</b>

* La funcionalidad para seleccionar automáticamente SBSAR al seleccionar un objeto no funciona en este momento, por lo que está desactivada.

## Add-on 2.0.0

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
