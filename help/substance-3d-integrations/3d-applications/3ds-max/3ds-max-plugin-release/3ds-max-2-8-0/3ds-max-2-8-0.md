---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/3d-applications/3ds-max/3ds-max-plugin-release-notes/3ds-max-2-8-0.html"
breadcrumb-title: ''
description: Revise las notas de la versión 2.8.0 del plugin 3ds Max para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Substance 3D Integrations
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3ds Max 2.8.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---


# 3ds Max 2.8.0

<b>Agregado/actualizado:
</b>

* Compatibilidad con la visibilidad condicional de los parámetros (&#39;visible if&#39;); los parámetros ahora se ocultarán cuando no se cumplan las condiciones y sus grupos respectivos permanecerán visibles.
* Se ha actualizado Corona Renderer a la versión 10 en el plugin 3ds Max, lo que mejora las capacidades de procesamiento y
* La última actualización mejora significativamente la velocidad de procesamiento y el uso de la CPU en 3ds Max 2024 al utilizar Substance, lo que alinea su rendimiento más estrechamente con la eficacia observada en 3ds Max 2022.

<b>Corregido:</b>

* Se ha mejorado el plugin del Substance para restringir los valores de entrada de teclado dentro del rango práctico de cada parámetro, lo que evita problemas con el control del regulador y los ajustes de valores manuales.
* Se ha resuelto un problema por el que la copia de conversiones de texturas de Substance2 (.sbsar) en el Editor de material de pizarra provocaba instancias no deseadas del nodo copiado, lo que podía provocar bloqueos relacionados con d3d11.dll.
* Se ha resuelto un problema de bloqueo en 3ds Max al procesar sustancias de materiales copiados personalizadas o editadas (.sbsar) con Corona Interactive.
* Se ha corregido un problema en el nodo Substance2 de 3ds Max por el que los reguladores de los valores de enteros 3 y 4 no respondían y solo la entrada numérica manual actualizaba los valores. Además, estos valores se mostraban incorrectamente en formato flotante. Los reguladores ahora son funcionales y reflejan con precisión los tipos de valor previstos.
* Se solucionó un problema en 3ds Max 2021 con Corona Render en el que los materiales de Substance aparecían correctamente en la ventana gráfica pero se procesaban como grises cuando los archivos se transferían a otro equipo. Los usuarios ya no necesitan configurar materiales desde cero ni cargar ajustes preestablecidos para un procesamiento adecuado.
* Se ha resuelto un problema de bloqueo en el plugin 3ds Max al intentar duplicar nodos de Substance en el Editor de material de pizarra.
* Se ha resuelto un problema por el que la configuración Límite de núcleos de CPU del plugin Substance no se guardaba después de reiniciar 3ds Max, lo que garantiza que los valores configurados por el usuario persistan ahora en las sesiones.

Esta versión se ha lanzado para 3ds Max 2021, 2022 y 2023
