---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/modo/working-with-normals.html"
breadcrumb-title: ''
description: Configure los ajustes de orientación normal del mapa en MODO para garantizar la correcta representación normal del mapa con materiales Substance.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Working with Normals
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trabajo con normales
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# Trabajo con normales

Trabajo con datos normales: definición de la orientación correcta

Los Substance de Stock están diseñados para usar la orientación normal de DX. Sin embargo, MODO utiliza OGL. Puede voltear la normal estableciendo el parámetro Formato normal en 1.0. El complemento Substance solo interpretará los parámetros establecidos en el Substance. Es posible que encuentre un Substance que no tenga el parámetro &quot;normal\_format&quot;, ya que depende del autor del Substance agregar este control a los Substance personalizados. Si encuentra un Substance que no tenga este parámetro, puede voltear el canal verde en la capa de textura del mapa normal para corregir la orientación.

>[!NOTE]
>
> La inversión del canal verde solo se produce si el Substance tiene una orientación normal incorrecta y el autor no ha creado un control para invertir la orientación normal en los parámetros del Substance

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../assets/normal-1.png)

</td>
<td style="border: 0;" valign="top">

![](../../../assets/invert-2.png)

</td>
</tr>
</table>
