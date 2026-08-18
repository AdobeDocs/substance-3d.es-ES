---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/renderers/keyshot.html"
breadcrumb-title: ''
description: Utilice materiales de Substance en el procesador de imágenes principales para la visualización de productos con mapas de textura exportados.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Keyshot
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Keyshot
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 8%

---


# Keyshot

*Keyshot 6.1.72*[&#x200B; Descargar Escena De Ejemplo](https://www.dropbox.com/s/rvjsbbcx7c74aah/keyshot.zip?dl=0)

## Exportación de Substance Painter

1. Para Keyshot, necesitará configurar un ajuste preestablecido de exportación usando Difusión, Reflejo, Metálico, Rugosidad y Normal (X directa).

   ![](https://helpx-prod.scene7.com/is/image/HelpxProd/key-01?$png$&jpegSize=300&wid=1794)

## Configuración avanzada de materiales

Utilizarás 2 materiales avanzados. Uno será para metálico y el otro para dieléctrico.

1. Establezca el material en Avanzado y cree un gráfico del material.

   **Metálico:**\
   a. Definir el índice de refracción en 10\
   b. Establezca los mapas como se indica en la tabla siguiente

   | Textura Substance Painter | Canal de materiales avanzado |
   | --- | --- |
   | Difusión | Difusión |
   | Metálico | Opacidad |
   | Normal | Bump \*Normal activado |
   | Rugosidad | Rugosidad |
   | Reflejo | Especular |

1. Crear un nuevo material avanzado

   **Dieléctrico:**\
   a. Establezca el Índice de refracción en 1,5\
   b. Establezca los mapas como se indica en la tabla siguiente

   | Textura Substance Painter | Canal de materiales avanzado |
   | --- | --- |
   | Difusión | Difusión |
   | Normal | Bump \*Normal activado |
   | Rugosidad | Rugosidad |
   | Reflejo | Especular |

1. Tome la salida del Material Avanzado Metálico y añádalo al + del Material Avanzado Dieléctrico. Esto creará un campo Etiqueta en el material.

   ![](../../assets/key-02.png)
