---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/upgrading-projects-known-issues.html"
breadcrumb-title: ''
description: Obtenga información sobre la actualización de proyectos de Unity con materiales de Substance y problemas conocidos que debe evitar durante la migración.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Upgrading ProjectsKnown Issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Actualizar proyectosProblemas conocidos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---


# Actualización de proyectos/problemas conocidos

>[!WARNING]
>
> El complemento Substance 3D para Unity 3.0.0 no admite la compatibilidad con versiones anteriores. Por lo tanto, asegúrese de utilizar Unity 2020.3.27x y versiones superiores.
> 
> Unity cambió la arquitectura de compilación predeterminada a x86 en lugar de x86\_64.\
> Los scripts no se ejecutarán si hacen referencia a Substance. Tendrá que volver a cambiar a x86\_64 y la compilación funcionará.

## Problemas conocidos

* &quot;*Error de aserción en la expresión&quot; al navegar por las carpetas del panel.*
  * Se trata de un error que se produce en el extremo de Unity cuando se realizan cambios en la interfaz de usuario, normalmente cambios en la miniatura, que deberían ser un mensaje inofensivo.
* *Las entradas de imagen parecen estar bloqueadas a 8 bits*
  * Esto se corrigió en la versión 3.8.0-3. El flujo de trabajo correcto sería que los usuarios cambiaran el formato predeterminado de Unity para la textura a RGBA64. El plugin se encargará de enviar correctamente esa información al Substance Engine.
