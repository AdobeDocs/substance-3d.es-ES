---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/bakers-settings/curvature-from-mesh-deprecated.html"
breadcrumb-title: ''
description: Referencia para el baker Curvatura desde malla obsoleto. En su lugar, utilice el baker Curvatura actualizada de Malla .
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

La Curvatura del baker de malla genera una textura de curvatura a partir de mallas de alto contenido de poli. Es más lento que el baker base de [curvatura](../../bakers-settings/curvature/curvature.md), pero produce resultados más precisos.

**Disponible en:**

* Substance Designer
* Substance Automation Toolkit

>[!NOTE]
>
> Desde Substance Designer 2019.3, este baker ha quedado obsoleto, por lo que recomendamos utilizar en su lugar el nuevo baker [Curvature from mesh](../../bakers-settings/curvature-from-mesh/curvature-from-mesh.md) .

## Parámetros

| *Parámetro* | *Descripción* |
| --- | --- |
| **Intensidad** | Qué tan fuertes serán los detalles de curvatura. Este parámetro está deshabilitado si **Saturación suave** está habilitado. |
| **Suave** **Saturar** | Si se activa, los detalles de curvatura se suavizarán. |
| **Maximizar rango** | Si se activa, los detalles de curvatura se ajustarán dentro de la capacidad del rango de textura. Esto significa que los valores muy fuertes se definirán como el máximo y todos los demás valores se escalarán de acuerdo con ese extremo. |
