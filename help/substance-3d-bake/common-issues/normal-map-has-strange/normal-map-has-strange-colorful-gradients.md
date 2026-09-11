---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/common-issues/normal-map-has-strange-colorful-gradients.html"
breadcrumb-title: ''
description: Corrija degradados extraños y coloridos en los mapas de normales comprobando las normales de malla, los grupos de suavizado y la asignación de UV.
helpx_creative_field: ""
helpx_description: bakers > Common Issues > Normal map has strange colorful gradients
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: El mapa de normales tiene degradados de colores extraños
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---


# El mapa de normales tiene degradados de colores extraños

El resultado del baker es un conjunto de degradados de colores muy intensos.

![](../../assets/color-gradient.png)


## Explicación

Los degradados de colores suelen producirse cuando hay una discrepancia entre la malla de alto y bajo contenido de poli durante el proceso de hace un bake. Este desajuste se puede explicar por la siguiente razón:

* Las mallas de alto y bajo poli <b>no se superponen</b> correctamente (vea la imagen siguiente).
* El alto-poli es <b>falta geometría</b> que el bajo-poli trata de cubrir.
* La malla de alta o baja densidad tiene vértices normales invertidos.

Cuando sucede, el proceso de hacer un bake intenta hacer coincidir la geometría que no existe, lo que da como resultado algo vacío. El baker rellena esta área vacía con un color extraído de los píxeles vecinos en las texturas, lo que crea el degradado colorido (a menos que <b>Difusión</b> esté deshabilitado).

## Solución

Dadas las pocas razones posibles que conducen a la no superposición entre las mallas, deben considerarse algunas soluciones:

* Asegúrese de congelar/restablecer la transformación de la malla (restablecer la forma x, etc.) para asegurarse de que todas las mallas son coherentes
* Importa la malla de alta y baja densidad en tu software de modelado en 3D para verificar que se superponen correctamente
* Asegúrese de que la convención de nomenclatura sea válida si está utilizando la característica [Coincidencia por nombre](../../features/matching-by-name/matching-by-name.md) (puede comprobarla haciendo un bake y, a continuación, buscando en el archivo de registro que debe imprimir los nombres de malla).

### Ejemplo

A continuación se muestra un ejemplo con una esfera de alto y bajo contenido de poli. A la izquierda, las mallas no se superponen porque se ha desplazado el alto-poli :

![](../../assets/baking-gradients.jpg)
