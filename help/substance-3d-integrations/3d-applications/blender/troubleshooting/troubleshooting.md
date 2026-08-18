---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/3d-applications/blender/troubleshooting.html"
breadcrumb-title: ''
description: Diagnostique y resuelva problemas comunes con el complemento Substance 3D en Blender mediante la consola del sistema.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Blender > Troubleshooting
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Resolución de problemas
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 0%

---


# Resolución de problemas

La consola del sistema se puede utilizar para diagnosticar los errores encontrados al utilizar el complemento. La ventana de consola del sistema de Blender se abre de forma diferente según el sistema operativo. Para obtener instrucciones detalladas, siga los pasos de la consola del sistema de Blender [página de documentación](https://docs.blender.org/manual/en/2.79/advanced/command_line/introduction.html#console-window-status-and-error-messages). La salida de la consola puede resultar útil cuando se producen problemas inesperados, como que las texturas no se carguen o los materiales se atasquen en el procesamiento.

Para informar de un error, únete al canal #substance-blender-beta en el [servidor Substance Discord](https://discord.com/invite/substance3d) o visita las [comunidades de Adobe](https://community.adobe.com/t5/substance-3d-plugins/ct-p/ct-substance-3d-plugins?page=1&sort=latest_replies&lang=all&tabid=all&topics=label-blender). En los informes se puede incluir la información pertinente del registro de la consola y los pasos de reproducción del problema.

## Problemas comunes y soluciones

* *Errores de consola relacionados con WMIC.*
  * *Ocasionalmente, las instalaciones de Windows no incluirán WMIC, lo cual es necesario en este caso. Así es como puede corregir esto manualmente:*
    * Vaya a Configuración - Sistema - Funciones opcionales
    * Seleccione &quot;Ver funciones&quot; y, a continuación, seleccione &quot;Agregar función de opción&quot;
    * Esto abrirá una nueva ventana, desplácese hacia abajo por la lista para encontrar WMIC, marque la casilla de verificación, luego presione siguiente, en la siguiente ventana presione Agregar.
    * Ahora debe dirigirse a una nueva ventana que muestra el progreso de la instalación de WMIC en acciones recientes.
    * *Tenga en cuenta que esta operación puede tardar unos minutos en descargarse. Después de esto, restablezca su computadora y reinicie Blender y el complemento. Al hacer clic en la carga en el panel Substance 3D, ahora debería mostrarse la ventana del explorador de archivos.*
  * Si esto no resuelve el problema, es posible que también necesite definir WMIC en sus variables PATH. Consulte la documentación de su versión específica de Windows.
* *No aparecen todas las configuraciones en el panel Substance 3D después de actualizar el complemento y cargar un material.*
  * Esto puede ocurrir al eliminar una versión anterior del complemento e instalar una versión más reciente en la misma sesión, ya que es posible que los archivos más antiguos se almacenen en la memoria caché del sistema.\
    El reinicio de Blender debe permitir que los cambios surtan efecto.
* *Problemas al instalar el complemento./ Los materiales se bloquean al procesarse entre sesiones. / Los materiales no generan texturas entre sesiones. / Errores al cargar archivos .sbsar.*
  * Esto puede ser un problema con la instalación de las herramientas de integración y normalmente se soluciona eliminando manualmente las herramientas. Visita la página [Desinstalando el complemento](../../../3d-applications/blender/uninstalling-the-add-on/uninstalling-the-add-on.md) para obtener instrucciones de eliminación manual.
* *Los materiales no se actualizan en la vista de procesamiento Ciclos*.
  * De forma predeterminada, el complemento no actualiza las texturas en la vista de procesamiento Ciclos. Sin embargo, se pueden actualizar a la fuerza habilitando <b>Ciclos Actualización automática de texturas</b> en las preferencias del complemento.
* Los parámetros parecen revertirse después de guardarlos en la vista de procesamiento Ciclos .
  * Se trata de un problema conocido de almacenamiento en caché en el lado de Blender que es solo visual. Al guardar, no se envía ningún mensaje al motor remoto para actualizar los archivos de textura generados. Las texturas aparecerán normales después de salir de la vista de procesamiento Ciclos y volver a ella.
* *Los materiales ya no se actualizan después de deshacer o cambiar los parámetros.*
  * Los materiales pueden no actualizarse después de deshacer las acciones. Aunque los parámetros volverán al estado anterior, las texturas no se desharán para que coincidan. Para actualizar la textura de nuevo, utilice el botón Actualizar para devolver los parámetros a los valores por defecto y volver a cargar las texturas.
* *Los colores definidos en Substance Designer aparecen de forma ligeramente diferente en el selector de color de Blender y los valores de color no son los mismos.*
  * Blender aplica una corrección de gamma a los colores solo del selector de color de Blender. Aunque esto provoca una discrepancia en el selector de color, los colores que aparecen en las texturas son precisos para los valores establecidos en las aplicaciones de Substance.
* Error de consola *&quot;no se reconoce wmic&quot; al cargar un material en Windows.*
  * Este problema se produce cuando C:\Windows\System32\wbem\ no se incluye en las variables del sistema PATH. Consulte la documentación de su versión específica de Windows.
* *Error &quot;Tipo de CPU incorrecto ejecutable&quot; en Mac.*
  * Este problema se produce cuando Rosetta no está habilitado en equipos Mac con ARM. Consulte la [página Rosetta de Apple](https://support.apple.com/en-us/102527) para obtener más información. Además, consulta esta [guía de instalación](https://medium.com/@jithmisha/fix-for-macbook-air-m1-m2-bad-cpu-type-in-executable-error-3719a0a1cb6) para obtener más instrucciones.
* *Las modificaciones en el gráfico de sombreado se deshacen al utilizar el botón Actualizar o al actualizar parámetros.*
  * El complemento actualizó las conexiones en el gráfico después de realizar cambios o actualizaciones. Para solucionar esto, duplique el material de la licuadora creado a partir del archivo .sbsar y asígnele un nuevo nombre. Agregue los nodos sólo al duplicado. Las texturas se actualizarán en el grupo de nodos mientras se mantienen los nodos agregados por el usuario. Al actualizar, copie estos nodos y péguelos de nuevo en un nuevo gráfico después de la actualización.
