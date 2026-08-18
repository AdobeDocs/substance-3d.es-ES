---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-4-4.html"
breadcrumb-title: ''
description: Revise las notas de la versión 2.4.4 del plugin Unity para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.4.4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.4.4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---


# Unity 2.4.4

Publicado en febrero de 2020

* Añadido: Asistencia técnica adecuada para 2019.3: Se han corregido los cambios en la API Unity que dañaban el objeto de scripts del complemento Substance. Objetos reprocesados para trabajar con las actualizaciones de la API 2019.3. Arreglado: el uso de material personalizado hace que el material se vuelva negro al salir de la reproducción
* Corregido: se produce un bloqueo al utilizar la función Duplicate() en un script, al entrar y salir de la reproducción.
* Fijo: restablecimiento del mosaico de materiales, la configuración y el sombreador en 2019.3
* Fijo: el sombreador de materiales HDRP no actualiza los cambios de un parámetro
* Fijo: el mapa de máscara HDRP no se actualiza
* Fijo: Añadir parámetro de cadena para la función Duplicar
* Solucionado: se ha corregido el soporte de Linux en la última estable de Unity
* Solucionado: problema de dirección de código de bits que debe desactivarse para iOS

Problemas conocidos:

* Si cambia el nombre del recurso HDRP, el plugin no generará un mapa de máscara.
* Al utilizar el plugin Substance en un proyecto HDRP, el uso de la compresión Raw establece texturas en escala de grises en Alpha8.
* Los objetos de juego se deseleccionarán en el modo de reproducción
* Al hacer clic en &quot;Generar mapas Mip&quot; en un gráfico del Substance en modo Reproducir y cambiar los parámetros, se produce un bloqueo infinito.
