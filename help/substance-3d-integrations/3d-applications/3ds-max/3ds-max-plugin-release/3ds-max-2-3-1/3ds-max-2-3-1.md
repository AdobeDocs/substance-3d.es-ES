---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/3d-applications/3ds-max/3ds-max-plugin-release-notes/3ds-max-2-3-1.html"
breadcrumb-title: ''
description: Revise las notas de la versión 2.3.1 del plugin 3ds Max para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > 3ds Max Plugin Release Notes > 3ds Max 2.3.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3ds Max 2.3.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 0%

---


# 3ds Max 2.3.1

Publicado el 13 de febrero de 2020

El complemento ahora se instala fuera del directorio 3ds Max en C:\ProgramData\Autodesk\ApplicationPlugins\SubstanceIn3dsMax. Ahora debería funcionar en cualquier lugar donde se le indique a 3ds Max que busque complementos, por lo que ahora debería funcionar instalado en una unidad de red, etc.\
Tenga en cuenta que el cambio al Complemento de la aplicación y el cambio del directorio de instalación hacen que una actualización de las versiones 2.1.1 y anteriores no funcione correctamente. Estos deben eliminarse manualmente para 3ds Max 2018 y 2019. La versión 2.2.0 debe actualizarse correctamente.\
Para algunos de los problemas que no se tratan en esta versión, se ha previsto otro pronto para solucionar estos y cualquier otro problema que pueda surgir.

Esta versión está disponible actualmente para 3ds Max 2018, 2019, 2020 y 2021.

* La barra de carga ahora busca primero en la carpeta de imágenes del proyecto
* El cuadro de diálogo de compatibilidad de procesador solo aparece ahora para el procesador de archivos VRay RT y VUE
* Arrastre y suelte para el Editor de material de pizarra desactivado para eliminar problemas con el lote Máx.
* El cuadro de diálogo Procesar ya no se muestra en el modo silencioso Máx. 3ds
* Los scripts de python más pequeños ahora son compatibles con Python 3
* Se ha agregado la compatibilidad con el Iniciador de Substance para enviar los recursos del Substance Source a 3ds Max. Esto requerirá cambios en el Iniciador, pero el soporte en el plugin estará allí a medida que se añada la función.
* El script del procesador Redshift ahora utiliza los nuevos nombres de nodo establecidos en Redshift 2.6.24
* Max ya no se bloquea cuando se asigna una ruta de acceso vacía a Substance2 SubstanceFilePath
* Eliminar la colisión de nombre del tipo SubstanceOutput con el plugin antiguo
* Se cambió el nombre de la clase SubstanceOutput a Substance2Output
* Se ha cambiado el nombre de la clase Substance Menu Manager a Substance2MenuManager
* Los ID de bloque de parámetros ahora se borran por la fuerza al abrir una escena, lo que elimina colisiones entre archivos de escena. Esto debería solucionar problemas con bloques de parámetros no válidos al cargar cuando se alterna entre escenas. La importación puede seguir teniendo problemas, ya que requiere cambios más complejos
* El complemento ahora se instala fuera de 3ds Max. Todas las rutas de acceso se han cambiado a relativas desde la ubicación de carga.
* El complemento ahora utiliza el sistema de complementos de la aplicación Autodesk.
