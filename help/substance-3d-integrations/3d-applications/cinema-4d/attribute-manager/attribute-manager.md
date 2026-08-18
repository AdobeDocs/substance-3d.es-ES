---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/3d-applications/cinema-4d/attribute-manager.html"
breadcrumb-title: ''
description: Utilice el Administrador de atributos de Cinema 4D para configurar las propiedades de los recursos del Substance y la configuración de los materiales.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Cinema 4D > Attribute Manager
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Administrador de atributos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---


# Administrador de atributos

Hay un nuevo modo para los recursos de Substance en el Administrador de atributos de Cinema 4D.

Cuando se selecciona un Substance en Substance Asset Manager, el Administrador de atributos cambia automáticamente al modo de Substance de activos. También puede cambiar manualmente a este modo en el menú de modo del Administrador de atributos.

En el modo de recursos de Substance tiene acceso a todas las entradas de un Substance y también tiene una descripción general de todos los canales de salida.

![](../../../assets/cinema-4d-9.png){width="500px"}

## Agrupación de entradas de Substance

Si se agrupan las entradas de un Substance, estos grupos se mostrarán como tales en el Administrador de atributos. Hay dos grupos predefinidos: **Propiedades básicas** y **Entradas de imagen**.

* En el grupo Propiedades básicas, se mostrarán todas las entradas que no se hayan asignado a un grupo en Substance Designer.
* Como su nombre ya lo sugiere, todas las entradas de Substance vinculadas a imágenes externas se recopilan en el grupo Entradas de imagen.

## Parámetro de nombre de archivo

Mediante el parámetro Filename del Administrador de atributos, se puede cambiar la ubicación de archivo de los recursos de Substance después de cargarlos en una escena.

![](../../../assets/cinema-4d-10.png){width="500px"}

Esto puede resultar útil no solo para reubicar archivos de Substance, sino también para intercambiar un Substance con otro completamente diferente.

En este caso, se preguntará al usuario si alguna referencia existente a canales de salida de Substance anteriores debe reasignarse al nuevo Substance.

![](../../../assets/cinema-4d-11.png){width="500px"}

Si la pregunta se responde con &#39;No&#39;, los vínculos al Substance anterior se eliminarán de todos los sombreadores de Substance. Para reasignar los canales de salida, el plugin buscará primero los canales de salida con el mismo tipo y luego con el mismo nombre.

## Parámetro Tri-state

Si se seleccionan varios Substance al mismo tiempo, las entradas compartidas entre estos Substance se mostrarán en tres estados y se podrán editar simultáneamente para todos los Substance seleccionados (al igual que todos los demás parámetros de Cinema 4D).

En estos casos, los canales de salida se mostrarán como se muestra a continuación.

![](../../../assets/cinema-4d-12.png){width="300px"}
