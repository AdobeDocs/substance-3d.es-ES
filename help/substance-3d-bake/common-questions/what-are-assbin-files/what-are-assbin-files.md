---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/common-questions/what-are-assbin-files.html"
breadcrumb-title: ''
description: Aprenda qué son los ficheros Assbin y cómo se utilizan como ficheros de caché de geometría para acelerar las operaciones de hace un bake.
helpx_creative_field: ""
helpx_description: "bakers > Common Questions > What are Assbin files "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'Qué son los archivos Assbin '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---


# ¿Qué son los archivos Assbin?

>[!WARNING]
>
> **Pregunta**
> 
> Después de hacer un bake en Substance Painter, encontré uno o varios archivos junto a mis mallas de alta densidad con la extensión de archivo &quot;assbin&quot;, ¿qué son? ¿Puedo eliminarlos de forma segura?

>[!NOTE]
>
> **Solución**
> 
> Asigne archivos a versiones preprocesadas de las mallas de alta densidad utilizadas durante el proceso de hace un bake. Son más rápidos de leer que los archivos de malla originales, lo que permite volver a hornear más rápido cuando se itera en la configuración de Bakers. Se pueden extraer de forma segura. El Substance Painter los regenerará si es necesario. Sin embargo, esto puede afectar a la hace un bake de actuaciones.
> 
> Es posible no generar nunca estos archivos entrando en las [preferencias principales](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/general-71008262.html) del Substance Painter y deshabilitando la opción &quot;Guardar archivos de escena preprocesados&quot;.
