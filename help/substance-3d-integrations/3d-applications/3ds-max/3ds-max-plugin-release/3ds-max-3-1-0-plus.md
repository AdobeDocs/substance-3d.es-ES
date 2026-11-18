---
description: Revise las notas de la versión del plugin 3ds Max 3.0.0 y posteriores para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
title: 3Ds Max 3.1.0+
source-git-commit: 28a9d8cf7a4eed4163f99e8158c9cb8f9da88302
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%
---

# 3ds Max 3.1.0+

## 3ds Max 3.1.1

**Fecha de publicación:** 18 de noviembre de 2026

**Compatible con:** 3ds Max 2025 y versiones posteriores

### Añadido/actualizado

* Actualización del Substance Engine (9.6.1.1) incluidas las correcciones de seguridad
* Compatibilidad de OpenPBR para 3ds Max 2025, 2026 y 2027 (Arnold y V-Ray)

### Limitaciones conocidas

* Peso de la emisión: El parámetro mission_weight no forma parte de la especificación OpenPBR 1.1 y no se conecta automáticamente. Después de aplicar el flujo de trabajo, defina manualmente el valor de Peso de emisión en el nodo OpenPBR si el material utiliza emisión.
* Diferencias visuales entre los procesadores: Alguna variación entre la previsualización de material en Substance 3D Designer y el resultado procesado en Arnold o V-Ray se debe a las diferencias en la implementación de cada procesador de la especificación de OpenPBR y mejorará a medida que converjan las implementaciones.
* Archivos SBSAR exportados de Substance 3D Painter 12.2.0. o anteriores pueden no conectarse correctamente al utilizar un flujo de trabajo de OpenPBR

## 3ds Max 3.1.0

**Fecha de publicación:** 18 de noviembre de 2026

**Compatible con:** 3ds Max 2024

### Añadido/actualizado

* Actualización del Substance Engine (9.6.1.1) incluidas las correcciones de seguridad
