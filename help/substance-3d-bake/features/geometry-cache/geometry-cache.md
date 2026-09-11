---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/features/geometry-cache.html"
breadcrumb-title: ''
description: Utilice el almacenamiento en caché de geometría para conservar los datos de malla preprocesados y acelerar significativamente las operaciones de hace un bake posteriores.
helpx_creative_field: ""
helpx_description: bakers > Features > Geometry Cache
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Caché de geometría
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---


# Caché de geometría

Al hacer un bake, las mallas se preprocesan para limpiarlas y convertirlas en un formato compatible con el proceso de hacer un bake. La caché de geometría es una forma de conservar esta geometría preprocesada de forma que se vuelva a cargar rápidamente para evitar rehacer esta operación más adelante (a menos que cambie la malla de origen).

* En **Substance Designer**, la caché de geometría se crea después de ejecutar una primera hace un bake. A continuación, la memoria caché se mantiene en memoria hasta que se cierra la ventana de baker.
* En **Substance Painter**, la caché de geometría se guarda como un archivo con la extensión **assbin** junto al archivo de origen después de la primera conversión.

La reutilización de la caché de geometría acelera bastante el proceso de hace un bake, especialmente al ajustar la configuración del baker para lograr el resultado perfecto.
