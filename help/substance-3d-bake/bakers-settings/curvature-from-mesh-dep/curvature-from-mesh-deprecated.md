---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/bakers-settings/curvature-from-mesh-deprecated.html"
breadcrumb-title: ''
description: Referencia de la curvatura obsoleta del panel Malla. Utilice en su lugar la Curvatura actualizada del panadero de mallas.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Curvature from Mesh (deprecated)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Curvatura desde malla (obsoleto)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# Curvatura desde malla (obsoleto)

La curvatura de malla baker genera una textura de curvatura a partir de mallas de alto contenido de poli. Es más lento que el panadero de base [curvatura](../../bakers-settings/curvature/curvature.md), pero produce resultados más precisos.

**Disponible en:**

* Substance Designer
* Substance Automation Toolkit

>[!NOTE]
>
> Desde Substance Designer 2019.3, este panadero está obsoleto y recomendamos usar la nueva panadería [Curvature from mesh](../../bakers-settings/curvature-from-mesh/curvature-from-mesh.md) en su lugar.

## Parámetros

| *Parámetro* | *Descripción* |
| --- | --- |
| **Intensidad** | Qué tan fuertes serán los detalles de curvatura. Este parámetro está deshabilitado si **Saturación suave** está habilitado. |
| **Suave** **Saturar** | Si se activa, los detalles de curvatura se suavizarán. |
| **Maximizar intervalo** | Si se activa, los detalles de curvatura se ajustarán dentro de la capacidad del rango de textura. Esto significa que los valores muy fuertes se definirán como el máximo y todos los demás valores se escalarán de acuerdo con ese extremo. |
