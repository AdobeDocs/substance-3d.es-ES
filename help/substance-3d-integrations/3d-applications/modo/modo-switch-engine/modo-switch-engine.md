---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/3d-applications/modo/modo-switch-engine.html"
breadcrumb-title: ''
description: Cambie entre los motores de CPU y Substance de GPU en MODO para optimizar el rendimiento en función del hardware.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Modo Switch Engine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Motor de cambio Modo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---


# Motor de cambio Modo

## Substance Engine de conmutación

Hay dos versiones del Substance Engine, la CPU y la GPU. El motor de GPU se utiliza para crear texturas superiores a 2K. El motor de CPU solo es capaz de generar texturas de hasta 2K. Si necesita texturas de mayor resolución, debe cambiar al motor de GPU.

Vaya a la opción Ajustes del Substance en el menú Kit de Substance y elija Cambiar de Substance Engine. Deberá reiniciar MODO para que el motor de GPU se active. Esta configuración actúa como una preferencia global. El motor de GPU se activará cada vez que ejecute MODO hasta que se cambie manualmente.

>[!NOTE]
>
> **El uso del motor de GPU Substance requiere una GPU con ram de vídeo dedicado de 1 GB o más. No se admiten las GPU integradas.**\
> Nvidia: GeForce 650M 1 GB o superior\
> AMD: 6870M o superior

![](../../../assets/switch.png)
