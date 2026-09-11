---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/getting-started/software-interface/substance-3d-designer.html"
breadcrumb-title: ''
description: Aprenda a acceder y utilizar la ventana de cocción en Substance 3D Designer para hornear información de modelos en texturas.
helpx_creative_field: ""
helpx_description: bakers > Getting Started > Software Interface > Substance 3D Designer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance 3D Designer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 2%

---


# Substance 3D Designer

![](../../../assets/sd-mesh-right-click.png)

Se puede tener acceso a la ventana para hornear a través del archivo de malla en la ventana del [Explorador](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html). Haga clic con el botón derecho en el nombre de la malla y elija &quot;**Información del modelo de horno**&quot; para abrir la ventana de horno.

## Información general

![](../../../assets/sd-window-overview.png){width="500px"}

La ventana para hornear de se divide en varios paneles que se describen a continuación.

### Elemento a hornear

![](../../../assets/sd-mesh-selection.png)

Este panel controla qué parte de la malla de baja polietileno se utilizará para realizar la cocción.

Este panel mostrará la geometría que se encuentra dentro del fichero de malla de baja densidad. De forma predeterminada, la lista se basa en los materiales individuales que se encuentran en el archivo, pero se puede cambiar a submallas en su lugar cuando sea pertinente. Puede anular la selección de los elementos que deben omitirse durante el proceso de cocción.

### Salida

![](../../../assets/sd-output.png)

Este panel controla dónde se ubicará la textura horneada.

| *Parámetro* | *Descripción* |
| --- | --- |
| **Método** | Controla cómo se almacenarán las texturas horneadas con el paquete de Substance.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Incrustado</strong> : la textura horneada se almacena en una subcarpeta junto al paquete Substance con un nombre específico.</li><li data-preserve-html="true"><strong>Vinculado</strong> (predeterminado) : la textura horneada se almacena en la carpeta definida y, a continuación, se hace referencia a ella en el Substance empaquetado.</li></ul> |
| **Carpeta** | Ubicación de las texturas horneadas al guardarlas. Haga clic en el botón de tres puntos para abrir un cuadro de diálogo de archivo y elija la carpeta de exportación. Aparecerá una marca de verificación a la derecha para indicar si la carpeta realmente existe o no. |
| **Nombre** | Convención de nomenclatura de las texturas horneadas. Haga clic en el botón de tres puntos para abrir un menú desplegable e insertar otros marcadores de posición (nombre de fondo, personalizado, material, malla). |
| **Ejemplo** | Simule un nombre de archivo para probar la convención de nomenclatura. |
| **Colocar recurso en una carpeta específica de malla** | Si se activa, las texturas horneadas se guardarán dentro de una carpeta denominada archivo de malla. |

### Mallas de alta definición

![](../../../assets/sd-high.png)

Este panel controla la lista de mallas de alta densidad y los ajustes relacionados. Consulte los [parámetros comunes](../../../bakers-settings/common-parameters/common-parameters.md) para obtener más información.

### Valores predeterminados

![](../../../assets/sd-default-values.png)

Consulte los [parámetros comunes](../../../bakers-settings/common-parameters/common-parameters.md) para obtener más información.

### Lista de panaderos y configuración

![](../../../assets/sd-baker-list.png)

El panadero es donde puedes elegir qué textura horneada quieres generar. De forma predeterminada, la lista está vacía.

* **Agregando un nuevo panadero:** Haga clic en el botón &quot;Agregar panadero&quot;.
* **Quitando un panadero:** Selecciona el panadero en la lista, luego haz clic en el botón &quot;Eliminar panadero&quot;.
* **Mover un panadero a la parte superior:** Seleccione el panadero en la lista y, a continuación, haga clic en el botón &quot;Tire hacia arriba&quot;.
* **Bajando por un panadero:**Seleccione el panadero en la lista, luego haga clic en el botón &quot;Empujar hacia abajo&quot;.

Cada panadero en el hereda de forma predeterminada los valores predeterminados (véase más arriba). El tamaño (resolución), por ejemplo, se puede anular haciendo clic en la celda de la línea del panadero. Esto es cierto para los demás ajustes de la línea.

Al hacer clic en un panadero de la lista, la vista Parámetros de panadero se actualizará con sus parámetros específicos.

Para obtener más información sobre los parámetros específicos, consulte: [Configuración de panaderos](../../../bakers-settings/bakers-settings.md).
