---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/3ds-max/troubleshooting.html"
breadcrumb-title: ''
description: Diagnostique y resuelva problemas con el complemento Substance en 3ds Max mediante el Listener de scripts para mensajes de error.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > Troubleshooting
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Resolución de problemas
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 1%

---


# Resolución de problemas

Scripting Listener se puede utilizar para diagnosticar los errores encontrados al utilizar el complemento. Para abrir el listener de script, vaya a Menú de scripts > Listener de scripts. Cuando se produce un error durante el uso del complemento, se imprime un mensaje de error correspondiente en esta ventana del Listener de scripts. Visite la [documentación oficial del editor de scripts](https://help.autodesk.com/view/3DSMAX/2023/ENU/?guid=GUID-C8019A8A-207F-48A0-985E-18D47FAD8F36) para obtener más información.

Para informar de un error, únete al canal #3dsmax-plugin en el [servidor Substance Discord](https://discord.com/invite/substance3d) o visita las [comunidades de Adobe](https://community.adobe.com/t5/substance-3d-plugins/ct-p/ct-substance-3d-plugins?page=1&sort=latest_replies&lang=all&tabid=all&topics=label-autodesk3dsmax). En los informes se puede incluir la información pertinente del registro de la consola y los pasos de reproducción del problema.

## Problemas conocidos

* *Si se reemplaza un archivo .sbsar que usa una salida difusa por un archivo .sbsar que no usa una salida difusa, se genera una representación en negro debido a la desconexión de la difusión que falta.*
  * Este es el comportamiento esperado para nodos de salida múltiples. En lugar de cargar estos .sbsars utilizando el mismo nodo, se recomienda utilizar nodos de Substance diferentes para cada uno.
