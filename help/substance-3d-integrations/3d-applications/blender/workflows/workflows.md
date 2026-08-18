---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/3d-applications/blender/workflows.html"
breadcrumb-title: ''
description: Aprenda a utilizar materiales de Substance con los procesadores Ciclos de mezclador y Eve para diferentes flujos de trabajo.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Blender > Workflows
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flujos de trabajo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---


# Flujos de trabajo

## Trabajo con ciclos

De forma predeterminada, los cambios de parámetro no se actualizan automáticamente en la ventana gráfica 3D cuando se visualizan en la vista de procesamiento Ciclos. Para ver las actualizaciones en la vista de procesamiento Ciclos, habilite **Ciclos Actualización automática de texturas** en Preferencias para forzar la actualización.

## Archivos multigraph .sbsar

El complemento admite archivos .sbrar con varios gráficos de sustancias. Al cargar un archivo con varios gráficos, aparecerá una nueva lista desplegable Gráficos en el panel Substance 3D. A diferencia de otros cambios de parámetros, el cambio de gráficos no actualizará automáticamente el material. Debido a esto, se debe usar el botón **Aplicar** para asignar de nuevo el material después de cambiar los gráficos.

>[!NOTE]
>
> Por defecto, el botón Aplicar añade el material en una nueva ranura sin anular las asignaciones de material anteriores. Elimina materiales anteriores o utiliza el menú desplegable de materiales para reasignar los materiales recién aplicados.

![](https://helpx-prod.scene7.com/is/image/HelpxProd/blender-workflows-multigraphs?$png$&jpegSize=100&wid=168)

## Trabajo con entradas de imagen

Cuando utilice un material de Substance que permita entradas de imagen personalizadas, un parámetro de selección de imagen en el panel Substance 3D le permitirá abrir el explorador de archivos de una imagen (icono de ) o seleccionar una imagen que exista en el proyecto (menú desplegable de icono de imagen).

La preferencia Exportar formato de imagen se puede utilizar para guardar las entradas de imagen generadas en Blender en la carpeta temporal. Consulte la página [Preferencias](../../../3d-applications/blender/preferences/preferences.md)para obtener más información.

![](../../../assets/blender-workflows-image-inputs-steps.png)

## Ajustes preestablecidos de red de sombreador.

El ajuste preestablecido de sombreado se puede ajustar rápidamente mediante el menú desplegable de la sección Salidas del panel Substance 3D. Estos ajustes preestablecidos de sombreado ajustan la forma en que se aplican las texturas de imagen.Ciclos/Estándar de evento utiliza la asignación de coordenadas de textura UV normal. Los otros tres ajustes preestablecidos de proyección Ciclos/Eva utilizan la asignación de coordenadas de textura generada para los métodos de proyección de cuadro, esfera o cilindro.

El ajuste preestablecido de sombreado predeterminado utilizado por los materiales se puede seleccionar en el complemento [Preferencias](../../../3d-applications/blender/preferences/preferences.md).

![](../../../assets/2022-08-12-12-12-33-adobeexpress-1.gif)

## Filtrado y ajuste de salidas

La sección Salidas del panel Substance 3D también dispone de opciones para filtrar las salidas. Se pueden utilizar tres botones junto a la lista desplegable de ajustes preestablecidos de sombreado para filtrar por salidas activadas (marca de verificación), salidas de sombreado (esfera) y todas las salidas disponibles (líneas).

Las salidas se pueden activar individualmente mediante la casilla de verificación. Cuando se habilita una salida, se crea la salida correspondiente en el grupo de nodos de textura. Si el nodo de material de Principled BSDF soporta ese resultado, se conectará automáticamente a él. El height se conectará a un nodo de desplazamiento y la Oclusión de ambiente se combinará con el color base en un nodo MixRGB.\
El menú desplegable de formato de archivo situado junto a la marca de verificación se puede utilizar para establecer el tipo de archivo con el que se guarda la textura de salida.

Además, las preferencias de salida de archivo predeterminadas se pueden cambiar en el complemento [Preferencias](../../../3d-applications/blender/preferences/preferences.md).

## Intercambio de materiales en objetos

Haga clic en el icono de esfera en el panel de propiedades de material de Blender para abrir una lista de materiales en su proyecto de Blende. Los materiales de Substance que se hayan creado en el panel también aparecerán en la lista. Al seleccionar un material de esta lista, se reemplazará el material activo en esa ranura de material.

## Desplazamiento

El desplazamiento de la malla de las texturas se admite en el procesador Ciclos , pero no en Eve. Para ver el desplazamiento, asegúrese de que la salida del Height esté activada. El complemento establecerá automáticamente la configuración de desplazamiento del material en **Desplazamiento y relieve**. Al visualizar el material en un objeto, ahora se mostrará el desplazamiento en la vista de procesamiento. La escala de desplazamiento se puede ajustar en el panel de materiales o en el nodo de desplazamiento.

Para obtener los mejores resultados, utilice niveles de subdivisión más altos o mallas de alto contenido de polietileno para materiales con detalles de desplazamiento complejos.
