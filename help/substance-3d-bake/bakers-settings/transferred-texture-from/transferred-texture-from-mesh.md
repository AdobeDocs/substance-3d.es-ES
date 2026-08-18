---
helpx_url: "https://helpx.adobe.com/substance-3d-bake/bakers-settings/transferred-texture-from-mesh.html"
breadcrumb-title: ''
description: Transfiere texturas entre mallas en función de sus UV, incluida la compatibilidad con las conversiones de mapas normales.
helpx_creative_field: ""
helpx_description: bakers > Bakers Settings > Transferred Texture from Mesh
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Textura transferida de malla
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 3%

---


# Textura transferida de malla

La textura transferida de mesh baker permite convertir una textura de una malla a otra en función de sus respectivos UV. Este panadero también soporta la transferencia o mapas normales (que requieren conversiones especiales). Para que funcionen, ambas mallas necesitan definiciones UV.

**Disponible en :**

* Substance Designer
* Substance Automation Toolkit

## Parámetros

| *Parámetro* | *Descripción* |
| --- | --- |
| **Archivo de textura** | Ruta al archivo de textura de entrada que se transferirá. |
| **Conjunto UV** | UV de malla para usar en la malla de alta densidad de poli para leer la textura y proyectarla sobre la malla de baja densidad de poli. |
| **Modo de filtrado** | Define cómo se debe realizar la interpolación de píxeles de la textura.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Más cercano</strong>: Sin interpolación, utilice el píxel más cercano encontrado a una posición determinada. Preciso, pero puede crear un suavizado.</li><li data-preserve-html="true"><strong>Bilineal</strong> (predeterminado): Utilice los cuatro píxeles más cercanos a una posición determinada. Sin suavizado, pero puede ser borroso.</li></ul> |
| **Mapa normal** | Si se habilita, indica al panadero que la textura de entrada que se va a transferir es un mapa normal. Esto indica que el panadero debe aplicar conversiones especiales a la textura para que sea compatible con la malla de destino. |
| **Tipo de mapa** | Define qué tipo de mapa normal es la textura de entrada.Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>Espacio mundial</strong></li><li data-preserve-html="true"><strong>Espacio tangente</strong> (predeterminado)</li></ul> |
| **Orientación normal** | Define el formato normal de la textura de entrada si **Map Type** está establecido en **Tangent Space**. Valores posibles:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>OpenGL</strong></li><li data-preserve-html="true"><strong>DirectX</strong> (predeterminado)</li></ul> |
