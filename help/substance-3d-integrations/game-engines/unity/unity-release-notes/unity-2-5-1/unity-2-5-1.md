---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-5-1.html"
breadcrumb-title: ''
description: Revise las notas de la versión 2.5.1 del plugin Unity para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.5.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.5.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---


# Unity 2.5.1

Publicado el 21 de mayo de 2020

Añadido

* Compatibilidad con la canalización de procesamiento universal: Las texturas Substance utilizarán automáticamente sombreadores y materiales URP

Fijo

* Configuración de resolución máxima del motor de CPU del Substance:
  * Se ha actualizado el nombre del campo en el menú Ajustes del Substance de &quot;Abrazadera de textura \*\*&quot; a &quot;Resolución máxima del motor de CPU del Substance&quot;.
  * Se mostrará una notificación de advertencia que indica que todos los materiales de Substance se volverán a importar cuando se modifique la configuración
* Se quitó el mensaje de depuración innecesario que se mostraba al instalar (&quot;TextureClamp = 4096 Unity.Engine.Debug:Log(Object)&quot;)
* Proyecto HDRP: Las propiedades de los materiales que se encuentran en los materiales estándar y HDRP se conservarán cuando se importen paquetes que incluyan Substance
* Las máscaras de reflejo y HDRP se crearán y funcionarán del modo esperado cuando se importe un material de Substance de un paquete de Substance que estaba en la versión anterior de Unity
* El material de Substance duplicado será el color deseado y ya no será amarillo al utilizar la función duplicar
* El origen del Substance se cargará como se esperaba después de cerrar y volver a abrir Unity
* Se bloquea al importar un paquete en un proyecto HDRP (de forma intermitente)
* El regulador funciona del modo esperado para los materiales de Substance con un parámetro expuesto que tiene el Editor establecido en Color (escala de grises)
* Se produce un bloqueo al hacer clic en &quot;Restablecer ajuste preestablecido a los valores predeterminados&quot; con gráficos de Substance que no tienen una resolución predeterminada.
* Bloqueo al cambiar el tamaño de salida de un material de Substance cuando no se muestra el parámetro de tamaño de salida
* La creación para iOS no fallará
* Las secuencias de comandos que utilizan materiales de Substance se ejecutarán al generar para Windows independiente
