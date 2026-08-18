---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-4-0.html"
breadcrumb-title: ''
description: Revise las notas de la versión 2.4.0 del plugin Unity para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.4.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.4.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# Unity 2.4.0

>[!WARNING]
>
> Unity cambió la arquitectura de compilación predeterminada a x86 en lugar de x86\_64.\
> Los scripts no se ejecutarán si hacen referencia a Substance. Tendrá que volver a cambiar a x86\_64 y la compilación funcionará.

## Nuevas funciones:

* Se ha añadido compatibilidad con proyectos HDRP (previsualización)
* Preferencias añadidas en el menú Substance
* Se ha añadido la capacidad de establecer la configuración predeterminada de importación de resolución del Substance
* Se ha añadido la capacidad de establecer la compresión Normal predeterminada
* Se ha agregado la capacidad de generar todos los resultados al importar un Substance
* Compatibilidad con salidas + salidas personalizadas con el mismo uso
* Configuración de resolución de plataforma añadida
* Se ha agregado la compatibilidad con IL2CPP

### Correcciones de errores:

* Se ha corregido un error que hacía que abrir Substance Source en el sistema operativo Mac generara un error de Linux
* Menor tiempo que se tarda en cambiar de plataforma. La conversión de texturas para plataformas móviles ahora se realiza en la versión de compilación en lugar de al cambiar de plataforma de destino.
* Error de aserción al importar sbsar
* La actualización de proyectos mediante .NET 3.5 provoca la interrupción de los materiales de Substance
* La fuente del Substance no es compatible con el diálogo de Linux que aparece en OS X
* El cambio de nombre de gráfico destruye los prefijos y el archivo de escena en el modo de serialización ForceText
* Los materiales de Substance con múltiples salidas que utilizan el mismo uso romperán El plugin no admite salidas personalizadas en sbsar

### Problemas conocidos:

* Al actualizar un proyecto de 2017-2018/2019, después de que el usuario importe el complemento de Substance, debe reiniciar Unity para actualizar el proyecto.\
  Solución alternativa: Cree un paquete de los activos/proyecto e impórtelo en un proyecto más nuevo con el complemento 2.4.0. Los archivos del Substance deben convertirse correctamente.
* Unity ha cambiado la arquitectura de compilación predeterminada a x86. Actualmente, el complemento Substance solo admite x86\_64.

**Ya No Es Totalmente Compatible:**

* Substance Live Link se ha eliminado del paquete de la tienda de recursos. (El paquete aún se puede descargar del Substance share)
