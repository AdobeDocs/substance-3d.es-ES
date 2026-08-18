---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/ambient-occlusion.html"
breadcrumb-title: ''
description: Aprenda a utilizar el Panadero de Oclusión ambiental para generar texturas de sombras ambientales mediante algoritmos rápidos acelerados por GPU.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Ambient Occlusion
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Oclusión ambiental
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 4%

---


# Oclusión ambiental

El panadero de Oclusión ambiental permite hornear una textura de sombra ambiental. Este panadero utiliza un algoritmo rápido ejecutado en la GPU.

**Disponible en:**

* Substance Designer
* Substance Automation Toolkit

>[!WARNING]
>
> * Es posible que este procesador no sea compatible con GPU antiguas.
> * El procesamiento en alta resolución en GPU de gama baja o móviles puede producir un bloqueo.

## Parámetros

| *Nombre* | *Descripción* |
| --- | --- |
| **Mapa normal** | Fichero de mapa normal de entrada que se puede utilizar para proporcionar detalles de geometría adicionales en la superficie de la malla que se deben tener en cuenta durante el cálculo del panadero. Este parámetro es opcional. |
| **Espacio mundial** | Si está activado, especifique que el mapa normal de entrada esté en Espacio mundial (en lugar de Espacio tangente). Si no se proporciona ninguna asignación normal de entrada, estos parámetros se omiten o se deshabilitan. |
| **Invertir normal** | Calcule el mapa de oclusión ambiental con normales invertidas (se puede utilizar para generar un mapa de thickness). |
| **Usar partes de malla no seleccionadas** | Utilice las partes de malla no seleccionadas de la malla para hornear el mapa de oclusión ambiental. |
| **Calidad** | Elija la calidad del mapa de Oclusión ambiental. Una calidad superior es más lenta de calcular.Valores disponibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Baja</strong> (paso 3)</li><li data-preserve-html="true"><strong>Medio</strong> (predeterminado, paso 5)</li><li data-preserve-html="true"><strong>Alta</strong> (10 pasada)</li><li data-preserve-html="true"><strong>Muy alto</strong> (16 Pass)</li></ul> |
| **Compensación de precisión** | Precisión de la oclusión ambiente. Un valor más bajo proporcionará una mayor precisión, pero puede producir artefactos más grandes. |
| **Desvanecimiento de distancia** | Extensión de la oclusión ambiental. |
