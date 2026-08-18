---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/common-issues/baker-output-is-fully-black-or-empty.html"
breadcrumb-title: ''
description: Solucione los problemas por los que las salidas de Baker son totalmente negras o vacías y aprenda a solucionar problemas de malla y UV.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Baker output is fully black or empty
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: La salida de Baker es totalmente negra o está vacía
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# La salida de Baker es totalmente negra o está vacía

>[!WARNING]
>
> **Problema**
> 
> El resultado de un panadero es una textura negra o vacía:
> 
> ![](../../assets/black.png)

>[!NOTE]
>
> **Explicación**
> 
> Una textura negra significa que el panadero no pudo encontrar la información requerida para generar un resultado. Por ejemplo, el proceso de cocción no encontró la malla de alto contenido de poli para que coincida con la de bajo contenido de poli, lo que no dio como resultado nada con lo que comparar.

>[!NOTE]
>
> **Solución**
> 
> * Compruebe si la malla de alta densidad necesaria para el panadero se ha cargado correctamente (consulte el archivo de registro/ventana para ver los errores).
> * Compruebe que las mallas de baja o alta densidad de poli no son demasiado grandes (más de un kilómetro) o demasiado pequeñas (menos de un centímetro).
> * Compruebe si el panadero pudo leer o procesar la malla (consulte el archivo de registro/ventana para ver los errores).
> * Compruebe si la característica [Coincidencia por nombre](../../features/matching-by-name/matching-by-name.md) no está configurada correctamente (algunos objetos pueden excluirse entre sí y nunca superponerse).
> * Verifique que los UV de bajo contenido de poli estén dentro del rango 0-1.
