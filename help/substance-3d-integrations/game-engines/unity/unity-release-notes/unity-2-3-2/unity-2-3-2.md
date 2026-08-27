---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-3-2.html"
breadcrumb-title: ''
description: Revise las notas de la versión 2.3.2 del plugin Unity para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.3.2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.3.2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---


# Unity 2.3.2

## Nuevas funciones:

* Serialización de materiales
* Reflejo: El complemento ahora permite importar archivos antiguos de Substance en paquetes (se actualiza automáticamente a los nuevos datos de Substance al importar)
* Las propiedades de los materiales se transfieren al importar los paquetes con datos del Substance
  * Nota: Esto solo se aplica a los paquetes creados con la actualización 2.3.0 o posterior
* Se ha añadido el botón Contornear textura al menú de gráficos del Substance

### Correcciones de errores:

* Se ha corregido un problema por el que el mosaico de material de Substance se restablecía si se eliminaba la carpeta Biblioteca
* Se ha mejorado la velocidad al salir del modo de reproducción
* Se ha corregido un bloqueo que se producía al actualizar el plugin mientras la DLL del Substance estaba en uso.
* La carpeta Allegorithmic ahora no se puede eliminar en Unity.
  * Nota: No se puede modificar el contenido de la carpeta Allegorithmic. Si se elimina dentro de Unity, pueden producirse varios problemas, lo que hace que la carpeta Allegorithmic vuelva a aparecer mágicamente cuando Unity se cierra y se vuelve a abrir. Ahora hay una advertencia que informa al usuario de que debe eliminarla con Unity cerrado manualmente desde la carpeta Assets del proyecto
* Se ha mejorado la velocidad al salir del modo de reproducción
* Se ha corregido un error que restablecía las propiedades del material de Substance cuando se quitaba la carpeta Biblioteca

## Problemas conocidos:

**Complemento del Substance principal**

* El usuario debe deshabilitar &quot;Habilitar Bitcode&quot; en el menú Configuración de compilación en Xcode para compilar para iOS
* Los Substance no trabajan con paquetes de recursos
* Los iconos de vista previa del Substance en el navegador de recursos cambian al icono del Substance S después de una reimportación

**Secuencias de comandos**

* Las secuencias de comandos no funcionan en tiempo de ejecución si el proyecto se establece en x86 en la configuración de generación
* Problemas al utilizar backend de scripts il2cpp con determinadas plataformas de compilación

**Substance Painter Live Link**

* Al crear un proyecto después de pintar con Substance Live Link, la malla pintada volverá al material predeterminado
* Canal AO no enviado con Painter Live Link
* Las mallas con varios materiales no funcionan en Unity Live Link
* La forma en que Unity LiveLink utiliza SimpleJson se bloquea con otras instancias de SimpleJson en un proyecto
