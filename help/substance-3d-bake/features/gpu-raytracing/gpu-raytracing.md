---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/features/gpu-raytracing.html"
breadcrumb-title: ''
description: Permite que el Trazado de rayos de GPU acelerado por hardware acelere el procesamiento de cálculos 25 veces o más para flujos de trabajo más rápidos.
helpx_creative_field: ""
helpx_description: bakers > Features > GPU Raytracing
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trazado de rayos de GPU
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 18%

---


# Trazado de rayos de GPU

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Algunos procesadores admiten la aceleración por hardware del trazado de rayos en la GPU, lo que normalmente aumenta la velocidad de cálculo en un factor de 25 o más.

## Requisitos de hardware

El trazado por rayos se activará automáticamente si el sistema cumple estos requisitos:

* Se ha instalado una GPU compatible\* (serie RTX, Titan V o GeForce 10xx)
* Los controladores de la GPU están actualizados
* Windows 10 &quot;Fall Creator&quot; / Actualización de octubre (versión 1809) o posterior instalada\*\*

</td>
<td style="border: 0;" valign="top">

Comparación de ![Trazado de rayos de GPU activado/desactivado](../../assets/rtx-ao-demo.gif "Comparación de Trazado de rayos de GPU activado/desactivado"){zoomable="yes"}

</td>
</tr>
</table>

\*: Las GPU NVIDIA compatibles incluyen todas las GPU que utilizan la arquitectura Pascal o más recientes. Es decir, la serie GTX 10, la serie Titan V, la serie RTX 20 o más reciente.

\*\*: Para comprobar tu versión de Windows, haz clic en el menú Inicio, escribe &#39;winver&#39; y pulsa Intro.\
Puede obtener la actualización a través de la [página dedicada](https://support.microsoft.com/en-us/help/4028685/windows-10-get-the-update) en el sitio web de asistencia de Microsoft.

>[!TIP]
>
> Si tiene problemas, puede desactivar el Trazado de rayos de GPU en las preferencias de la aplicación.

## Panaderos compatibles

En las tablas siguientes se enumera la compatibilidad del Trazado de rayos de GPU con cada panadero, según la versión de panadero de Substance 3D:

+++Versión 3 y superior

| Baker | Apoya al Trazado de rayos de GPU |
| --- | --- |
| Oclusión ambiental | <div><img alt="(marca)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Normal doblada | <div><img alt="(marca)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Color | <div><img alt="(marca)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Curvatura | <div><img alt="(marca)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Altura | <div><img alt="(marca)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Normal | <div><img alt="(marca)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Espacio de mundo de normales | <div><img alt="(error)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |



| Baker | Apoya al Trazado de rayos de GPU |
| --- | --- |
| Máscara de opacidad | <div><img alt="(marca)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Posición | <div><img alt="(marca)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Posición baja | <div><img alt="(error)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| Grosor | <div><img alt="(marca)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Textura transferida | <div><img alt="(marca)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| De mundo a tangente | <div><img alt="(error)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |


+++

+++Versión 2

| Baker | Apoya al Trazado de rayos de GPU |
| --- | --- |
| Oclusión ambiental | <div><img alt="(error)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| Oclusión ambiental de malla | <div><img alt="(marca)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> \* |
| Normales dobladas de malla | <div><img alt="(marca)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> \* |
| Color de malla | <div><img alt="(error)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> \* |
| Convertir UV a SVG | <div><img alt="(error)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| Curvatura de malla | <div><img alt="(marca)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> \* |
| Altura de malla | <div><img alt="(error)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> \* |
| Normal de malla | <div><img alt="(error)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> \* |



| Baker | Apoya al Trazado de rayos de GPU |
| --- | --- |
| Máscara de opacidad de la malla | <div><img alt="(error)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> \* |
| Posición de malla | <div><img alt="(error)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> \* |
| Posición | <div><img alt="(error)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| Grosor de malla | <div><img alt="(marca)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> \* |
| Textura transferida desde la malla | <div><img alt="(error)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> \* |
| Dirección espacial mundial | <div><img alt="(error)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| Normales espaciales mundiales | <div><img alt="(error)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |


\*: Admite trazado de rayos de CPU, que es significativamente más lento que el Trazado de rayos de GPU.

+++
