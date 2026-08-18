---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-4-5.html"
breadcrumb-title: ''
description: Revise las notas de la versión 2.4.5 del plugin Unity para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.4.5
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.4.5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---


# Unity 2.4.5

Publicado el 6 de abril de 2020

* Añadido: Comprobación de activos HDRP mediante la API 2019.3
* Añadido: Actualización de Substance Engine 7.2: corrige algunos materiales de Substance de Source que no funcionan
* Añadido: Actualizar la configuración de destino para que coincida con la resolución de CPU
* Añadido: Ajuste de resolución máxima del motor de la CPU (ajuste 4k o 2k)
* Añadido: Convertir Substance que no sean HDRP dentro de un proyecto HDRP
* Corregido: Bloqueo al importar una gran cantidad de Substance
* Corregido: Excepción al hacer clic en Reimportar en el modo de reproducción después de cambiar los parámetros del Substance
* Corregido: Validar la resolución de salida (textura) (API para limitar el motor de CPU a 2K) Preferencias del usuario para establecer el valor predeterminado en 4K
* Corregido: Al hacer clic en &quot;Generar mapas Mip&quot; en un gráfico del Substance en modo Reproducir y cambiar los parámetros, se produce un bloqueo infinito
* Corregido: Al utilizar el plugin de Substance en un proyecto HDRP, el uso de la compresión Raw define texturas en escala de grises como Alpha8
* Corregido: GameObject deseleccionado en el modo de reproducción
* Corregido: El mapa de rugosidad no se actualiza con el cambio de parámetro
* Corregido: La salida de máscara no se genera correctamente para algunos archivos de Substance en HDRP
* Corregido: Bloqueo al cambiar el menú desplegable de mapa alfa empaquetado entre dos opciones
* Corregido: La casilla de verificación Instanciación de GPU se desactiva al hacer clic fuera del material del Substance.
* Corregido: Cuando se utiliza la función Duplicate(), el gráfico del Substance duplicado no tiene el smoothness empaquetado correctamente en el alfa del metal.
* Corregido: Si se cambia el destino de compilación a Android, las texturas tendrán un formato incorrecto hasta que se vuelvan a importar manualmente.
* Corregido: Si se elimina un archivo de Substance en Unity, se producirá una excepción NullReferenceException.
* Corregido: Deshabilitar el uso de la API HDRP de Unity 2019.3 para versiones anteriores

Problemas conocidos:

* La casilla de verificación de emisión no está activada de forma predeterminada y el valor HDR se establece en negro al importar un Substance.
* Las propiedades de los materiales de los paquetes con materiales estándar de Substance no se trasladan a la importación.
* La actualización de 2017-2019/2020 no funciona en HDRP
* Al hacer clic en la opción 2048 clamp del menú de configuración y seleccionar 4096 en la configuración de destino (sin hacer clic en aplicar), se produce un error en el registro de la consola
