---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/renderers/color-management.html"
breadcrumb-title: ''
description: Comprender la gestión de color y la corrección de gamma cuando se usan materiales Substance con diferentes procesadores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Renderers > Color Management
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gestión de colores
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 2%

---


# Gestión de colores

Adoptaremos un enfoque simplista al afirmar que la representación del espacio lineal proporciona la matemática correcta para los cálculos de iluminación. Crea un entorno que permite representar las interacciones de la luz de una manera creíble en el mundo real. Para un debate sobre la representación del espacio lineal, debemos introducir el concepto de corrección gamma. Al codificar imágenes para su visualización y almacenamiento, la corrección gamma es el proceso de optimización para reducir el ancho de banda y la asignación de bits. Este proceso aprovecha la percepción del brillo del ojo humano, que sigue aproximadamente a la raíz cúbica de la luminancia.

>[!NOTE]
>
> El renderizado de espacios lineales es un tema muy complejo. Para obtener más información, consulta el [VOLUMEN UNO DE LA GUÍA DE PBR](https://academy.substance3d.com/courses/the-pbr-guide-part-1) en [Substance Academy](https://academy.substance3d.com/).

## Gestión de colores

El propósito de este documento es detallar el proceso de trabajo con texturas exportadas de **Substance Painter** y **Substance Designer** en [software 3D](https://www.adobe.com/es/products/substance3d/3d-augmented-reality.html) y renderizadores.

La forma correcta de interpretar una imagen utilizada como entrada en un canal de material depende de cómo se utilice la imagen en la escena. El espacio de color, la codificación y si los valores de color son proporcionales a la **luminancia de referencia en escena** o a la **luminancia de referencia en pantalla** también desempeñan un papel importante.

* Las imágenes utilizadas para representar **datos sin color** no se deben transformar. Estos son normalmente mapas de **oclusión normal**, **rugosidad**, **metálico**, **desplazamiento** y **ambiente**.**&#x200B;**
* Las imágenes que representan el color que vemos pueden tener varios escenarios. Por ejemplo, las imágenes que ya son **lineales para escenas** normalmente no necesitan convertirse, como las imágenes de **rango dinámico alto** almacenadas en formatos como **OpenEXR** y **HDR**.
* Las imágenes creadas para la visualización (**display-reference**) deberán tener su gamma eliminado. Estos incluyen la mayoría de formatos como **PNG**, **JPEG** y **BMP**. Estas imágenes son **base**, **color**, **difusa**, **specular** y **emisiva**.

Si bien se trata de una simplificación excesiva, puede resultar útil considerar el proceso de la siguiente manera:

* &quot;de referencia en escena (ej. lineal)&quot; : No aplicar una conversión
* &quot;de referencia en pantalla (ej. sRGB)&quot; : Aplique la transformación inversa para &quot;linealizar&quot; la imagen para realizar el cálculo adecuado

>[!NOTE]
>
> La función de decodificación sRGB (EOTF) que convierte el espacio gamma en espacio lineal se utiliza en Substance Painter y Substance Designer, y se define en el estándar IEC 61966-2-1:1999

El Substance Designer se puede configurar para usar [OpenColorIO](https://opencolorio.org/) para la administración de color. Esto te permite tener *transformaciones de color coherentes* y visualización de imágenes en varias aplicaciones. En este modo, Substance Designer trabajará internamente con colores **RGB lineal**. Dado que la profundidad de bits 8 no suele ser suficiente para representar colores lineales, se recomienda usar la profundidad *al menos* de **16 bits** para las texturas de color en el [gráfico](https://docs.substance3d.com/display/SDDOC/Graph+View).

![](https://helpx-prod.scene7.com/is/image/HelpxProd/sd-cm?$png$&jpegSize=200&wid=686)

Cuando presentamos [ACES](https://www.oscars.org/science-technology/sci-tech-projects/aces), ahora tenemos dos espacios de color diferentes, el sRGB lineal (la versión sin gamma de sRGB) y [ACEScg](https://acescolorspace.com/), que es un espacio de color de amplia gama (&quot;lineal&quot; o de referencia en escena) más adecuado para el procesamiento CG.

Gráfico de trazado de gama *-<https://acescolorspace.com/>*

El Substance Designer también admite **Adobe Color Engine (ACE)**. Con **ACE**, puedes elegir tu espacio de color de trabajo entre **sRGB**, **sRGB lineal** y **ACEScg**. Cuando se usa **sRGB**, **ACE** es más o menos igual que el modo heredado. Cuando se usa un espacio de color lineal, **ACE** se parece más o menos a [OpenColorIO](https://opencolorio.org/index.html).

## Plugins de Substance

Cuando se utilizan materiales de Substance mediante el plugin de Substance Integration, las salidas se marcan para lineales/gamma automáticamente mediante la integración y la gestión de color de la aplicación host. Sin embargo, es importante entender el proceso: cuando los mapas de Substance se utilizan como mapas de bits exportados en lugar de como materiales de Substance, es posible que deba marcar manualmente las texturas como **codificadas mediante gamma** o **raw**, según el procesador que esté utilizando. Normalmente, los archivos .png, .jpg, .tga o .tif de 8 o 16 bits tienen codificación gamma, mientras que los archivos **sRGB OETF** y .exr son lineales.

## Aplicaciones 3D

### Uso de texturas

* [Texturas Substance en maya](../../renderers/color-management/textures-in-maya/substance-textures-in-maya.md)
* [Texturas Substance en 3ds Max](../../renderers/color-management/textures-in-3ds-max/substance-textures-in-3ds-max.md)
