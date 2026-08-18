---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/modo/modo-plugin-release-notes/modo-v-2-7-0.html"
breadcrumb-title: ''
description: Consulte las notas de la versión del plugin MODO 2.7.0 para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Modo Plugin Release Notes > Modo v. 2.7.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Modo v. 2.7.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---


# Modo v. 2.7.0

* Numerosas correcciones de bloqueo
* Compatibilidad con flotador de 32 bits
* Texturas 4k en el motor de la CPU y texturas 8k en el motor de la GPU
* nuevo formato LPK para la versión del complemento
* nuevo menú Kit para el complemento Substance
* Compatibilidad con glTF/sombreador de principios para MODO 12.0
* Rutas relativas agregadas para archivos de Substance
* Compatibilidad con Linux
* Nueva interfaz de usuario para cargar y guardar ajustes preestablecidos
* Los ajustes preestablecidos incrustados se cargan desde Designer
* Cuadro de advertencia de memoria de GPU quitada
* Comandos de carga/guardado de ajustes preestablecidos editados

  Los nuevos comandos disponibles son:

  **substance.getsbsname** Convierte el identificador de un objeto substance en su nombre interno

  Todos ellos esperan un nombre interno adecuado adquirido de substance.getsbsname:

  **substance.setpreset** Establece el ajuste preestablecido actual de un Substance en el índice **substance.getpresetindex** Obtiene el índice preestablecido actual **substance.getpresetat** Devuelve el nombre de cadena de un ajuste preestablecido en un **index substance.getpresetcount** dado Devuelve el número de ajustes preestablecidos que tiene un Substance **substance.savepresetfile** Guarda un ajuste preestablecido de la configuración actual en la ruta de archivo dada **substance.loadpresetfile** Carga un archivo preestablecido preestablecido al Substance una ruta de archivo

  Comandos de IU:

  Comando de interfaz de usuario **substance.loadpresetui** para cargar un comando de interfaz de usuario **substance.savepresetui** preestablecido para guardar un comando de interfaz de usuario **substance.selectpresetui** preestablecido para establecer el ajuste preestablecido
