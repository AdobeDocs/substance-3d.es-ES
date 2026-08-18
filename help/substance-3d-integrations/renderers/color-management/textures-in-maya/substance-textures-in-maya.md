---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/renderers/color-management/substance-textures-in-maya.html"
breadcrumb-title: ''
description: Configure los ajustes del espacio de color para las texturas Substance en maya para garantizar una gestión y representación del color precisas.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Color Management > Substance textures in Maya
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Texturas Substance en maya
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# Texturas Substance en maya

El espacio de color que establezca para los mapas depende de la configuración y las reglas establecidas en [Configuración de administración de color maya](https://help.autodesk.com/view/MAYAUL/2020/ENU/?guid=GUID-B260195C-A0FE-4F51-9EA2-099B61B7725A).

El Substance del complemento Maya se establece en &quot;Ignorar reglas de archivo de espacio de color&quot; en el nodo de archivo. El complemento se ocupa de la configuración del espacio de color independientemente de la gestión de color, mediante el uso de lo siguiente:

BaseColor, Difuso, Emisor, Specular = sRGB\
Normal, height, desplazamiento, rugosidad, metálico = RAW

Normalmente, deberá establecer el espacio de color en RAW para las imágenes que representan datos que no son de color. Sin embargo, esta configuración puede verse afectada por las reglas que haya establecido en la gestión de color.

![](../../../assets/raw.png)
