---
helpx_url: 'https://helpx.adobe.com/es/substance-3d-bake/features/matching-by-name.html'
breadcrumb-title: ''
description: Utilice la función Correspondencia por nombre (Matching by Name) para aislar mallas de baja y alta densidad de poli y evitar que la geometría se desangre durante el proceso de cocción.
helpx_creative_field: ''
helpx_description: bakers > Features > Matching by Name
helpx_experience_level: ''
helpx_learn_topic: ''
helpx_tags: ''
title: Coincidencia por nombre
user-guide-description: ''
user-guide-title: ''
source-git-commit: d57629bee333101dd9f40f30ed24ff84b6b8c6f1
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 0%

---


# Coincidencia por nombre

![](../../assets/banner-matching-by-name.jpg)

Coincidencia por nombre es el nombre de un método de filtrado que se puede utilizar en Substance Bakers para aislar mallas de poli y poli altas y bajas en función de su nombre.

Esta funcionalidad es muy útil para evitar que la geometría se desangre entre sí durante el proceso de cocción para lograr texturas limpias. Evita tener que alejar las mallas (a menudo denominadas &quot;explosión&quot;) para lograr el mismo resultado.

## Cuándo utilizar la coincidencia por nombre

### Horneado normal del mapa con sangrado de malla

En este ejemplo, el casco de la parte superior de la cabeza del personaje se desvanece en la cara del personaje.

Al habilitar Coincidencia por nombre podemos ignorar el casco y hornear la cara correctamente. *Este resultado se basa en la configuración de coincidencia principal.*

| *Malla* | *Coincidencia por nombre de* | *Coincidencia por nombre en* |
| --- | --- | --- |
| ![](../../assets/baking-demo-vela.png){width="250px"} | ![](../../assets/baking-demo-vela-normal-nomatch.png){width="250px"} | ![](../../assets/baking-demo-vela-normal-withmatch.png){width="250px"} |

### Ignorar cara posterior para geometría flotante

En este ejemplo, los &quot;botones&quot; de la parte superior del cuadro son de geometría flotante, no están conectados a la malla de poli alta. Por lo tanto, proyectarán sombras por defecto en el cuadro situado debajo de ellas, que mostrará el borde geométrico.

Al habilitar Coincidencia por nombre para el ajuste **Ignorar cara posterior**, podemos hornear la oclusión ambiente mientras ignoramos el área debajo de los botones para que parezca un cuadro singular.*Este resultado se basa en el uso de la configuración Ignorar reverso.*

| *Malla* | *Coincidencia por nombre de* | *Coincidencia por nombre en* |
| --- | --- | --- |
| ![](../../assets/ignorebf-mesh.png){width="250px"} | ![](../../assets/ignorebf-off.png){width="250px"} | ![](../../assets/ignorebf-on.png){width="250px"} |

## Cómo Funciona La Coincidencia Por Nombre

El sistema Coincidencia por nombre (Matching By Name) funciona leyendo el nombre geométrico tanto en las mallas poly altas como en las bajas y utilizando una palabra clave (el sufijo) para identificar o hacer coincidir los nombres. De forma predeterminada, los panaderos utilizan el sufijo específico, pero pueden cambiarse (véase a continuación).

Los sufijos admitidos actualmente son:

| *Tipo de sufijo* | *Valor predeterminado* | *Uso* |
| --- | --- | --- |
| Poly alto | *\_high* | Se utiliza para aislar el nombre de la malla de poli alto para que coincida con el de poli bajo. |
| Poly bajo | *\_low* | Se utiliza para aislar el nombre de la malla de poli bajo para que coincida con el de poli alto. |
| Ignorar la cara posterior | *\_ignorebf* | Se utiliza para omitir las caras posteriores de los panaderos que utilizan rayos secundarios, como la Oclusión Ambiente.*Este sufijo debe estar presente únicamente en las mallas de alto contenido polivinílico, por ejemplo:**mesh\_high\_ignorebf*** |

Algunas reglas que se deben tener en cuenta para que esta función funcione correctamente:

* La coincidencia por nombre debe estar habilitada en [Parámetros comunes](../../bakers-settings/common-parameters/common-parameters.md), ya que está **desactivada de forma predeterminada**.
* Es posible que se habilite una configuración secundaria Coincidencia por nombre en algunos panaderos (como [Oclusión ambiental](../../bakers-settings/ambient-occlusion-from/ambient-occlusion-from-mesh.md)) porque producen rayos secundarios.
* La coincidencia es sensible a mayúsculas y minúsculas, esto significa que una malla llamada &quot;**Vela**&quot; no coincidirá con otra llamada &quot;**vela**&quot;.
* Se pueden hacer coincidir varias mallas en función de la posición del sufijo en el nombre de geometría.

A continuación se muestran ejemplos de cómo puede funcionar la coincidencia (utilizando el sufijo predeterminado):

| Nombre de poli bajo | Coincidirá Con High Poly | No Coincide Con La Alta Poly |
| --- | --- | --- |
| <ul data-preserve-html="true"><li data-preserve-html="true">body_low</li></ul> | <ul data-preserve-html="true"><li data-preserve-html="true">body_high</li><li data-preserve-html="true">body_high_top</li><li data-preserve-html="true">body_high_1</li><li data-preserve-html="true">body_high_2</li></ul> | <ul data-preserve-html="true"><li data-preserve-html="true">de cuerpo alto</li><li data-preserve-html="true">body_top_high</li></ul> |
| <ul data-preserve-html="true"><li data-preserve-html="true">Head_low</li></ul> | <ul data-preserve-html="true"><li data-preserve-html="true">Head_high</li></ul> | <ul data-preserve-html="true"><li data-preserve-html="true">head_high</li></ul> |
| <ul data-preserve-html="true"><li data-preserve-html="true">Leg_low_top</li></ul> | <ul data-preserve-html="true"><li data-preserve-html="true">Leg_high</li><li data-preserve-html="true">Leg_high_top</li><li data-preserve-html="true">Leg_high_high_top</li></ul> | <ul data-preserve-html="true"><li data-preserve-html="true">Leg_top_high</li></ul> |

## Cómo configurar los panaderos

### Activación de Coincidencia por Nombre

La coincidencia por nombre se puede habilitar en [Parámetros comunes](../../bakers-settings/common-parameters/common-parameters.md) de la configuración de Baker:

| *Software* | *Configurando configuración* |
| --- | --- |
| **Substance Painter** | <ol class="steps" data-preserve-html="true"> <li class="step" data-preserve-html="true">     Abra la ventana de cocción (a través de los ajustes del conjunto de texturas).    </li> <li class="step" data-preserve-html="true">     Mostrar los parámetros comunes.    </li> <li class="step" data-preserve-html="true">     Cambie la configuración <strong>Match</strong> de &quot;Always&quot; a &quot;By Mesh Name&quot;.<br/> <img data-preserve-html="true" src="../../assets/baking-match-setting-sp.png"/>    </li> </ol> |
| **Substance Designer** | <ol class="steps" data-preserve-html="true"> <li class="step" data-preserve-html="true">     Abra la ventana de horneado (haciendo clic con el botón derecho en una malla vinculada en la ventana del explorador).    </li> <li class="step" data-preserve-html="true">     Cambie la configuración <strong>Match</strong> de &quot;Always&quot; a &quot;By Mesh Name&quot;. <br/> <br/>    </li> </ol> |

### Cambio de los nombres de sufijo

Los sufijos predeterminados son \_low y \_high y se pueden cambiar de la siguiente manera:

* **Substance Painter**: En la [ventana de panadería](../../getting-started/software-interface/3d-painter/substance-3d-painter.md), dentro de los parámetros comunes.
* **Substance Designer**: En [Configuración del proyecto](https://experienceleague.adobe.com/es/docs/substance-3d-designer/using/workspace/preferences/project-settings), en Configuración de cocción.

## Mallas de alta densidad de zepillo

Las mallas de alta densidad exportadas desde zBrush se pueden utilizar para el procesamiento con la función Correspondencia por nombre, pero se pueden seguir algunos ajustes:

| *Formato de archivo* | *Descripción* |
| --- | --- |
| **FBX** | No hay parámetros específicos para habilitar/deshabilitar, los archivos de malla se pueden usar tal cual. |
| **OBJ** | Los archivos OBJ exportados por zBrush no funcionarán con **Coincidencia por nombre** de forma predeterminada. En su lugar, es posible indicar al Substance Painter que utilice el nombre de archivo de malla en lugar de hacerlo coincidir con las mallas por nombre.Para ello, asegúrese de lo siguiente:<ol data-preserve-html="true"><li data-preserve-html="true"><strong>Deshabilite</strong> el parámetro de grupo (Grp) para <strong>cada subherramienta</strong>.</li><li data-preserve-html="true"><strong>Asigne un nombre</strong> al archivo OBJ según corresponda (por ejemplo: <strong>body_high.obj</strong>).</li></ol> ![](../../assets/zbrush-setting.png) |
