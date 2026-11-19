---
description: Revise las notas de la versión 3.0.0 y posteriores del plugin Maya para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
title: Maya 3.0.0
source-git-commit: 6453364f7dafa75c5bb2531a8707257498953e23
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%
---

# Maya 3.1.0+

## Maya 3.1.1

**Fecha de publicación:** 18 de noviembre de 2026

**Compatible con:** Maya 2025 y versiones posteriores

### Añadido/actualizado

* Actualización del Substance Engine (9.6.1.1) incluidas las correcciones de seguridad
* Soporte de OpenPBR para Maya 2025, 2026 y 2027 (Arnold y V-Ray)

### Limitaciones conocidas

* Peso de la emisión: El parámetro mission_weight no forma parte de la especificación OpenPBR 1.1 y no se conecta automáticamente. Después de aplicar el flujo de trabajo, defina manualmente el valor de Peso de emisión en el nodo OpenPBR si el material utiliza emisión.
* OpenPBRs - V-Ray — Escala de radio subsuperficial: Al utilizar el flujo de trabajo OpenPBR - V-Ray, subsurface_radius_scale puede devolver un valor de 0. Si esto ocurre, quite la conexión y establezca el valor manualmente en el nodo V-Ray.
* Diferencias visuales entre los procesadores: Alguna variación entre la previsualización de material en Substance 3D Designer y el resultado procesado en Arnold o V-Ray se debe a las diferencias en la implementación de cada procesador de la especificación de OpenPBR y mejorará a medida que converjan las implementaciones.
* Archivos SBSAR exportados de Substance 3D Painter 12.2.0. o anteriores pueden no conectarse correctamente al utilizar un flujo de trabajo de OpenPBR.

## Maya 3.1.0

**Fecha de publicación:** 18 de noviembre de 2026

**Compatible con:** Maya 2024

### Añadido/actualizado

* Actualización del Substance Engine (9.6.1.1) incluidas las correcciones de seguridad
