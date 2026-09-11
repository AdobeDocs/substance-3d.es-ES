---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/maya/maya-plugin-release-notes/maya-2-2-1.html"
breadcrumb-title: ''
description: Revise las notas de la versión 2.2.1 del plugin Maya para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > Maya > Maya Plugin Release Notes > Maya 2.2.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maya 2.2.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# Maya 2.2.1

Maya 2.2.1 Versión:

* Actualizar Substance Engine a 8.3.0
* Añada compatibilidad nativa con Arnold, lo que elimina la necesidad de almacenar la caché en el disco
* Esto se puede usar después de habilitar la representación de extensiones en la configuración y reiniciar Maya
* Las versiones compatibles son:
* Maya 2017 - MtoA 3.1.0/Arnold 5.2.0
* Maya 2018 - MtoA 4.0.0/Arnold 6.0.0, MtoA 4.2.0/Arnold 6.2.0
* Maya 2019 - MtoA 4.0.0/Arnold 6.0.0, MtoA 4.2.0/Arnold 6.2.0, MtoA 5.0.0/Arnold 7.0.0
* Maya 2020: MtoA 4.0.0/Arnold 6.0.0, MtoA 4.2.0/Arnold 6.2.0, MtoA 5.0.0/Arnold 7.0.0
* Maya 2022 - MtoA 4.2.1/Arnold 6.2.0, MtoA 5.0.0/Arnold 7.0.0
* Directorio de instalación actualizado en Windows y MacOS
* Los archivos binarios en MacOS/Windows ahora se firman mediante certificados de Adobe
* Los conmutadores de canal ahora se ocultan cuando el autor de la barra lateral es Allegorithmic o Adobe, en lugar de Allegorithmic
* Se ha añadido una nueva interfaz de usuario de flujo de trabajo con funciones añadidas para duplicar, sobrescribir, cambiar de nombre y eliminar flujos de trabajo

Se han añadido los siguientes nuevos comandos de scripts:

substanciemaya

substanceGetEnableRenderingExtensions

substanceSetEnableRenderingExtensions

substance.workflow.py

substanceWorkflowIsReadOnly

substanceWorkflowRenameWorkflow

substanceWorkflowDuplicateWorkflow

substanceWorkflowOverwriteWorkflow

substanceWorkflowRemoveWorkflow

Correcciones de errores:

* Solucionar error al abrir el cuadro de diálogo Configuración
* Las funciones de flujo de trabajo ya no fallan cuando se genera una pyc

Esta versión está disponible para Maya 2017, 2018, 2019, 2020 y 2022 en Linux, MacOS y Windows, y Maya LT 2018, 2019 y 2020 en MacOS y Windows
