---
helpx_url: 'https://helpx.adobe.com/substance-3d-general/ecosystem/general-system-requirements.html'
breadcrumb-title: ''
description: Compruebe los requisitos del sistema de las aplicaciones de Substance 3D para asegurarse de que su hardware cumple con las especificaciones mínimas, recomendadas u óptimas.
helpx_creative_field: ''
helpx_description: General Knowledge > Ecosystem > General system requirements
helpx_experience_level: ''
helpx_learn_topic: ''
helpx_tags: ''
title: Requisitos generales del sistema
user-guide-description: ''
user-guide-title: ''
source-git-commit: eef3d78f33034f2c24f4c4471d9ccac805184525
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 2%
---

# Requisitos generales del sistema

## Requisitos de hardware

+++Windows

|  | Mínimo | Recomendado | Óptimo |
| --- | --- | --- | --- |
| **SO** | Windows 11 de 64 bits, versión 23H2 | Windows 11 Versión de 64 bits 24H1 | Windows 11 de 64 bits, versión 24H2 |
| **CPU** | Intel Core i5 AMD Ryzen 5 | Intel Core i7 AMD Ryzen 7 | Intel Core i9 AMD Ryzen 9 |
| **GPU** | NVIDIA GeForce RTX 2060 Super NVIDIA Quadro RTX 4000 AMD Radeon RX 5700 XT AMD Radeon Pro W5700 | NVIDIA GeForce RTX 3080 NVIDIA Quadro RTX A4000 AMD Radeon RX 6800 XT AMD Radeon Pro W7700 | NVIDIA GeForce RTX 4090 NVIDIA Quadro RTX 5000 Ada Generation AMD Radeon RX 7900 XTX AMD Radeon Pro W7800 |
| **VRAM** | 8 GB | 16 GB | 24 GB |
| **RAM** | 16 GB | 32 GB | 64 GB |
| **Almacenamiento** | SSD con 30 GB de espacio disponible | SSD con 50 GB de espacio disponible | SSD con 70 GB de espacio disponible |

+++

+++macOS

|  | Mínimo | Recomendado | Óptimo |
| --- | --- | --- | --- |
| **SO** | macOS 15 Sequoia | macOS 27 Golden Gate | macOS 27 Golden Gate |
| **CPU** | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| **GPU** | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| **RAM** | 16 GB | 32 GB | 64 GB |
| **Almacenamiento** | SSD con 30 GB de espacio disponible | SSD con 50 GB de espacio disponible | SSD con 70 GB de espacio disponible |

>[!WARNING]
>
> Para las canalizaciones creadas teniendo en cuenta la [plataforma de referencia VFX](https://vfxplatform.com/), las aplicaciones de Substance 3D se pueden instalar en macOS 14 Sonoma. Sin embargo, las aplicaciones de Substance ya no se prueban en versiones de sistemas operativos que no cumplan los requisitos mínimos del sistema, por lo que no se garantiza su estabilidad. Se recomienda actualizar a una versión más reciente del sistema operativo.

+++

+++Linux

|  | Mínimo | Recomendado | Óptimo |
| --- | --- | --- | --- |
| **SO** | **ETLA empresarial** RHEL 8.6 o posterior o RHEL 9.2 o posterior **Steam** Ubuntu 22.04.1 LTS | **ETLA empresarial** RHEL 8.6 o posterior o RHEL 9.4 o posterior **Steam** Ubuntu 22.04.1 LTS o posterior | **ETLA empresarial** RHEL 8.6 o posterior o RHEL 9.4 o posterior **Steam** Ubuntu 22.04.1 LTS o posterior |

**Red Hat Enterprise Linux (RHEL) 9.x**: El paquete xcb-util-cursor requerido por nuestras aplicaciones se eliminó del repositorio EPEL 9 el 10 de mayo de 2024. A partir de esta fecha, el paquete es compatible con el repositorio RHEL 9 predeterminado, coincidiendo con la versión de RHEL 9.4. Los clientes que utilicen versiones de RHEL anteriores a la 9.4 ya no podrán obtener el paquete xcb-util-cursor del repositorio EPEL 9 después del 10 de mayo de 2024.

Para obtener más información sobre la disponibilidad de este paquete en el repositorio RHEL 9 predeterminado, consulte: [Red Hat Enterprise Linux 9 - Manifiesto del paquete - Repositorio AppStream](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html-single/package_manifest/index#AppStream-repository)

Para obtener más información sobre este cambio, consulte: [Red Hat Bugzilla - Error 2238273](https://bugzilla.redhat.com/show_bug.cgi?id=2238273), [Red Hat Bugzilla - Error 2212302](https://bugzilla.redhat.com/show_bug.cgi?id=2212302)

+++

+++RV

| Marca | Modelos |
| --- | --- |
| Meta | Rift, Rift S, Quest, Quest 2 (con vínculo), Quest Pro |

+++

Para obtener más información, examine los requisitos de cada aplicación:

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../assets/sa-appicon-noshadow-256.png" alt="Icono de Substance 3D Sampler" width="64px"/><br><a href="https://experienceleague.adobe.com/en/docs/substance-3d-sampler/using/getting-started/system-requirements">Substance 3D Sampler</a></td>
    <td style="border: 0;" valign="top"><img src="../../assets/ds-appicon-noshadow-256.png" alt="Icono de Substance 3D Designer" width="64px"/><br><a href="https://experienceleague.adobe.com/en/docs/substance-3d-designer/using/getting-started/system-requirements">Substance 3D</a> <a href="https://experienceleague.adobe.com/en/docs/substance-3d-designer/using/getting-started/system-requirements">Designer</a></td>
    <td style="border: 0;" valign="top"><img src="../../assets/pt-appicon-noshadow-256.png" alt="Icono de Substance 3D Painter" width="64px"/><br><a href="https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/getting-started/system-requirements">Substance 3D Painter</a></td>
  </tr>
</table>

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../assets/md-appicon-noshadow-256.png" alt="Icono de Substance 3D Modeler" width="64px"/><br><a href="https://helpx.adobe.com/substance-3d-modeler/getting-started/system-requirements.html">Substance 3D Modeler</a></td>
    <td style="border: 0;" valign="top"><img src="../../assets/sg-appicon-noshadow-256.png" alt="Icono de Substance 3D Stager" width="64px"/><br><a href="https://helpx.adobe.com/substance-3d-stager/getting-started/system-requirements.html">Substance 3D Stager</a></td>
    <td style="border: 0;" valign="top"></td>
  </tr>
</table>

## Notas adicionales

### Configuración no admitida

* Las configuraciones de equipos Apple con eGPU y GPU instaladas por el usuario no son compatibles.
* Las máquinas virtuales de Windows no son compatibles.
* El sistema operativo Windows Server no es compatible.
