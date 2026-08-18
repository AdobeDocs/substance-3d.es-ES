---
helpx_url: "https://helpx.adobe.com/es/substance-3d-bake/common-questions/texture-baked-outside-of-substance-software-looks-incorrect.html"
breadcrumb-title: ''
description: Solucione los problemas de por qué las texturas horneadas en el software de Substance externo son incorrectas y aprenda a solucionar los problemas de espacio de color.
helpx_creative_field: ""
helpx_description: bakers > Common Questions > Texture baked outside of Substance software looks incorrect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: La textura horneada fuera del software del Substance parece incorrecta
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# La textura horneada fuera del software del Substance parece incorrecta

>[!WARNING]
>
> **Pregunta**
> 
> ¿Por qué la textura que horneé con una aplicación externa y no los Substance Bakers parecen incorrectos en Substance Painter?

>[!NOTE]
>
> **Solución**
> 
> No hay una solución inmediata a este problema ya que muchos factores pueden contribuir al problema :
> 
> * Compruebe que el formato normal entre el software del Substance y la aplicación externa es el mismo. OpenGL es [X+, Y+, Z+] y DirectX es [X+, Y-, Z+]
>   * En Substance Painter, el formato normal se puede cambiar en la [configuración del proyecto](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/interface/project-configuration).
>   * En Substance Designer, el formato normal se puede cambiar en las [preferencias del proyecto](https://experienceleague.adobe.com/en/docs/substance-3d-designer/using/workspace/preferences/project-settings).
> * Compruebe que la malla se ha triangulado antes de hornearla e importarla en el software del Substance. Consulte [esta página](../../guides/triangulating-before-bak/triangulating-before-baking.md) para obtener más información.
