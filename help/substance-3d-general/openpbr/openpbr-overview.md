---
title: OpenPBR
description: Obtenga más información sobre el Modelo de material de OpenPBR y cómo utilizarlo para el procesamiento basado en la física en aplicaciones 3D.
source-git-commit: 17ce332abf45d97c495c30b89df031ad2f2bbdf0
workflow-type: tm+mt
source-wordcount: '9657'
ht-degree: 0%

---


# OpenPBR

[**Descargar una versión sin conexión de esta página.**](../assets/openpbrf/openpbr.pdf)

**OpenPBR** es un modelo de sombreado de superficie abierto y basado físicamente diseñado para proporcionar una forma coherente y predecible de describir materiales en diferentes herramientas 3D, renderizadores y canalizaciones. Define un modelo de material único y completo capaz de representar una amplia gama de superficies del mundo real, al tiempo que sigue siendo lo suficientemente flexible como para admitir looks más estilizados o impulsados por el artista mediante parámetros físicamente significativos.

El modelo corrige incoherencias de larga data entre sombreadores &quot;estándar&quot; que se comportan de manera similar en el nombre pero difieren en las definiciones de parámetros y las suposiciones físicas entre las aplicaciones. Basado en los principios de la representación basada en la física, el OpenPBR describe los materiales en términos de comportamiento de la luz en el mundo real, haciendo hincapié en el ahorro de energía, rangos de parámetros intuitivos y respuestas de iluminación estable. En lugar de prescribir una interfaz de usuario específica, el OpenPBR define cómo se comportan los materiales a un nivel fundamental, lo que permite a las herramientas implementar el modelo a su manera, al tiempo que conserva resultados visuales coherentes a medida que los activos se mueven entre aplicaciones y canalizaciones.

Este documento es una guía orientada al artista para comprender y trabajar con el OpenPBR. Explica los principios subyacentes del modelo, cómo sus componentes describen el comportamiento de la luz en el mundo real y cómo esas ideas se traducen en la creación material práctica. En lugar de centrarse en una aplicación específica, la guía está pensada para artistas 3D que trabajen en áreas como el desarrollo de looks, la creación de texturas y la representación y que quieran crear materiales robustos y físicamente plausibles que sigan siendo coherentes y transferibles entre diferentes entornos de software.

>[!NOTE]
>
> Si ya estás trabajando con OpenPBR y estás buscando asistencia técnica, es posible que [las preguntas frecuentes del OpenPBR](openpbr-faq.md) ya tengan respuestas a tus preguntas.

![](../assets/OpenPBR_desk.jpg)

*Nikie Monteleone creó la escena de la demostración de OpenPBR de arriba. Celine Dameron creó representaciones de materiales y canales de ejemplo en este documento.*

## Interoperabilidad y estándares de archivos

### Un lenguaje material compartido con el OpenPBR

Uno de los objetivos principales del OpenPBR es mejorar la forma en que los materiales se mueven entre las herramientas. En lugar de ser un sombreado vinculado a un único procesador o aplicación, el OpenPBR define un **modelo de sombreado compartido**, una forma común de describir cómo responde un material a la luz.

Para los artistas, esto significa que un material de OpenPBR no es solo, por ejemplo, &#39;un material de Adobe&#39; o &#39;un material de Autodesk&#39;, sino más bien una descripción del comportamiento de la superficie y el volumen que, en principio, puede ser entendido por múltiples herramientas. La intención es que un material creado en una aplicación pueda interpretarse de forma coherente en otro lugar, siempre que esas herramientas sean compatibles con el modelo de OpenPBR.

### El problema del intercambio de activos

La especificación del OpenPBR reconoce explícitamente un desafío de larga data en la producción: Los **materiales no se transmiten bien entre aplicaciones**. Los diferentes renderizadores suelen utilizar nombres de parámetro, supuestos de sombreado y modelos subyacentes diferentes, lo que dificulta y lleva mucho tiempo hacer coincidir el aspecto.

El OpenPBR está diseñado como respuesta a este problema. Al definir un único modelo de material físicamente conectado a tierra que cubre las necesidades comunes de producción -metales, dieléctricos, materiales en capas, transmisión, dispersión-, proporciona un objetivo estable para el intercambio. Si bien esto no garantiza coincidencias visuales perfectas en todas las situaciones, reduce significativamente la ambigüedad en comparación con los modelos de sombreador patentados.

Para los artistas, la conclusión práctica es que el OpenPBR tiene como objetivo preservar la *intención*. Incluso cuando no es posible alcanzar una paridad visual exacta, la estructura del material -lo que es metal, lo que es transmisivo, lo áspera o anisotrópica que es una superficie- sigue siendo clara y transferible.

![](../assets/OpenPBR_meetmat.jpg)

### Relación con MaterialX

El OpenPBR está estrechamente vinculado a **MaterialX**, un framework estándar del sector para describir materiales y looks sin tener en cuenta el procesador. La implementación de referencia del OpenPBR se realiza dentro de MaterialX, lo que significa que los materiales del OpenPBR pueden representarse utilizando un formato de intercambio ya existente en muchas canalizaciones.

Esta relación es importante porque el OpenPBR en sí es **no un formato de archivo**. En su lugar, define *qué* es un material, mientras que MaterialX proporciona una forma estandarizada de *almacenar e intercambiar* ese material entre herramientas. En la práctica, esto permite integrar materiales de OpenPBR en descripciones de escenas más amplias y compartirlos entre los DCC y los renderizadores compatibles con MaterialX.

Para los artistas, esto suele ocurrir bajo el capó, pero explica por qué los materiales de los OpenPBRs se describen cada vez más como &quot;portátiles&quot; o &quot;interoperables&quot; en los gasoductos modernos.

### Qué significa y qué no significa la interoperabilidad

Es importante establecer expectativas realistas en torno a la interoperabilidad. El OpenPBR no garantiza que un material se vea idéntico en todas las aplicaciones. Las diferencias en la iluminación, los algoritmos de representación, la gestión del color y la compatibilidad de funciones pueden seguir afectando a la imagen final.

Lo que sí proporciona el OpenPBR es una base de referencia común: un conjunto coherente de parámetros y comportamientos, una comprensión compartida de cómo se construyen los materiales y una ruta más clara para transferir materiales entre herramientas sin reconstruirlos desde cero.

Para los artistas, esto supone menos sorpresas cuando los activos se mueven entre departamentos o aplicaciones, y un flujo de trabajo que enfatiza la lógica de materiales duraderos en lugar de los trucos específicos de herramientas.

### Implicaciones prácticas para los artistas

Desde una perspectiva cotidiana, trabajar con el OpenPBR fomenta hábitos que apoyan naturalmente la interoperabilidad:

* Pensar en términos de comportamiento de la luz en lugar de tipos de materiales específicos de la aplicación
* Uso de parámetros físicamente significativos (metalidad, rugosidad, transmisión, dispersión)
* Evitar la dependencia de soluciones no documentadas o específicas del procesador

Incluso cuando los materiales nunca abandonan una sola aplicación, estas prácticas se alinean con los estándares de desarrollo modernos, lo que hace que los activos estén más preparados para el futuro a medida que evolucionan las herramientas y los renderizadores.

## Tipos de materiales

### Materiales definidos por interacción con la luz

El OpenPBR es un modelo monolítico (un &#39;uber-shader&#39;) destinado a representar una amplia gama de tipos de materiales; estos tipos se describen en términos de cómo la luz interactúa con ellos. En lugar de definir materiales en términos de ajustes preestablecidos fijos como, por ejemplo, &quot;vidrio&quot; o &quot;piel&quot;, cada material de OpenPBR se crea a partir de un modelo de capas horizontales y verticales, que permite a los artistas combinar características totalmente definidas y físicamente significativas, como el reflejo difuso, la reflexión del specular, la transmisión, la dispersión subsuperficial y la superposición. Las diferentes combinaciones de estos comportamientos producen naturalmente materiales familiares del mundo real.

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/extra/lighting-condition/fabricLightingInteriorAtelier.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/extra/lighting-condition/fabricLightingStudio.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/extra/lighting-condition/fabricLightingTerraceNearGranaries.png" alt=""/></td>
  </tr>
</table>

Este enfoque utiliza un modelo fijo que define de antemano el esquema de capas y mezclas, eludiendo así cualquier exigencia para el artista de crear una red de sombreados caso por caso, y permite al OpenPBR representar materiales simples y complejos de una manera coherente y físicamente fundamentada.

![](../assets/openpbrf/model_schematic2.png) Haga clic para hacer zoom. *Figura adaptada de la especificación OpenPBR Surface, © Academy Software Foundation, usada bajo la licencia Apache 2.0*

### Comportamientos de materiales principales

Aunque el OpenPBR no impone tipos de materiales estrictos, la mayoría de los materiales del mundo real entran en unas cuantas categorías de comportamiento amplias. Comprender estas categorías puede ayudar a establecer un modelo mental sólido para los materiales de construcción.

### Materiales dieléctricos (no metálicos)

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/basecolor/baseColorViolet.png" alt=""/><br><em>Ejemplo de un material dielétrico.</em></td>
    <td style="border: 0;" valign="top">Los dieléctricos son materiales no metálicos como plástico, madera, piedra, tela, goma y piel. Sus características definitorias son:<br><br><ul><li>Un componente difuso visible</li><li>Reflejos de specular en su mayoría incoloro (blanco)</li><li>Reflectividad controlada principalmente por el Índice de Refracción (IOR)</li><li>Sin comportamiento de reflexión metálica</li></ul><br><br><strong>Parámetros clave para materiales dieléctricos:</strong><br><br><ul><li>Color base define el color general del material</li><li>El color del specular influye en el matiz de las iluminaciones del specular (más prominente en los ángulos de pastoreo)</li><li>Rugosidad del specular controla el aspecto de las iluminaciones de specular nítidas o desenfocadas</li><li>Peso del specular escala la intensidad general de los puntos más destacados del specular </li><li>En el caso de los materiales dieléctricos, el reflejo difuso domina el aspecto de la superficie y se controla mediante el color base. Los reflejos del specular son limitados en incidencia normal, y aumentan hacia ángulos de pastoreo, pero permanecen sin matices.</li></ul></td>
  </tr>
</table>

### Materiales metálicos

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/metalness/metalness1Colored.png" alt=""/><br><em>Ejemplo de un material metálico.</em></td>
    <td style="border: 0;" valign="top">Los materiales metálicos como el acero, el aluminio, el cobre o el oro se comportan de manera fundamentalmente diferente a los materiales no metálicos (dieléctricos). En el caso de los metales, la apariencia se basa casi exclusivamente en el reflejo del specular: a diferencia de los dieléctricos, los metales no tienen un componente difuso, y la luz no dispersión bajo la superficie sino que se refleja directamente. Sus características definitorias son:<br><br><ul><li>Ningún componente difuso: el color procede por completo del reflejo</li><li>Reflejos de specular de colores</li><li>El detalle de la superficie, especialmente la rugosidad, desempeña un papel importante en la apariencia</li></ul><br><br><strong>Parámetros clave para materiales metálicos:</strong><br><br><ul><li>Color base controla el color de los reflejos</li><li>Rugosidad del specular controla el grado de nitidez o desenfoque de los reflejos</li><li>Specular Escala de peso intensidad de reflexión</li></ul></td>
  </tr>
</table>

### Metalicidad base

Base Metalness define si un material se comporta como un dieléctrico o un metal: no se trata solo de un ajuste visual, sino de un cambio en la respuesta de luz subyacente del material.

* **0** → totalmente no metálico (difuso + specular)
* **1** → totalmente metálico (solo speculares)
* **0-1** → una combinación de ambos comportamientos. Los valores intermedios se utilizan mejor para mezclas de materiales como dirt, corrosión o superficies desgastadas, en lugar de materiales &quot;parcialmente metálicos&quot;.

#### Directrices prácticas para la metalurgia

* Use **0** o **1** para la mayoría de los materiales
* Utilice valores medios solo para superficies mixtas
* Confíe en la rugosidad y el detalle de la superficie para dar forma al aspecto metálico.

Utilice capas (por ejemplo, capa) en lugar de reducir el metal para metales pintados o recubiertos, transparentes y transmisivos.

### Materiales transparentes y transmisibles

Los materiales transparentes y transmisivos permiten que la luz pase a través de ellos. Algunos ejemplos comunes son el vidrio, muchos líquidos y plásticos claros o tintados. Sus características definitorias son:

* La luz entra en la superficie y sale del lado opuesto
* El thickness afecta fuertemente a la apariencia
* Refracción controlada por el Índice de Refracción (IOR) y afectada por la rugosidad de la superficie
* La refracción, la absorción, la dispersión y la dispersión dan forma al aspecto final

La transmisión describe cómo la luz atraviesa un objeto. Las áreas más gruesas aparecen más oscuras o saturadas, mientras que las áreas más finas aparecen más claras. Parámetros como Color de transmisión, Profundidad de transmisión, Color de Dispersión y Dispersión funcionan de forma conjunta para controlar este comportamiento.

Una distinción entre los términos &quot;transparente&quot; y &quot;transmisivo&quot;: &#39;transparente&#39; es un término cotidiano de la vida real; algo es transparente si podemos ver a través de él. &#39;Transmisivo&#39; es un sinónimo de &#39;translucidez&#39;. El vidrio esmerilado, por ejemplo, permite que la luz pase a través de él (y así, es transmisivo), pero no es transparente - no podemos ver a través de él.

### Materiales subterráneos

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/extra/subsurface-scattering/subsurfaceScattering.png" alt=""/><br><em>Ejemplo de un material que utiliza la dispersión subsuperficial.</em></td>
    <td style="border: 0;" valign="top">Los materiales subterráneos permiten que la luz entre en la superficie, que la dispersión se encuentre debajo de ella y que salga de nuevo cerca del punto de entrada. Algunos ejemplos comunes son la piel, la cera, el mármol y muchos materiales orgánicos, como muchos tipos de alimentos. - frutas, verduras o queso Saint-Nectaire, por ejemplo. Las características definitorias de los materiales subterráneos son:<br><br><br><ul><li>Sombreado suave y difuso</li><li>Sangrado de color en áreas finas</li><li>La apariencia depende del thickness</li><li>La luz no pasa a través del objeto</li></ul><br><br><br>La dispersión subsuperficial es distinta de la transmisión. Mientras que la transmisión describe la luz que pasa a través de un material y sale por el lado opuesto, la dispersión subsuperficial describe la luz que entra en una superficie, se dispersa dentro de esa superficie y luego sale en las proximidades del punto por el que entró, principalmente en el mismo lado. En particular, los materiales metálicos no admiten la transmisión ni la dispersión subsuperficial. El cambio del valor de transmisión o subsuperficie de un material completamente metálico (es decir, un material cuyo valor de Metalidad base es 1) no afectará a su aspecto.</td>
  </tr>
</table>

## Fusión entre comportamientos de materiales

Los materiales del mundo real rara vez son perfectamente puros. Muchas superficies se describen mejor como mezclas de comportamientos, en lugar de pertenecer a una sola categoría. Por ejemplo, si una superficie muestra signos de dirt, desgaste o óxido, distintas partes de la superficie reaccionarán a la luz de diferentes maneras. El OpenPBR soporta esto permitiendo mezclar suavemente, de una parte de una superficie a otra.

### Metalness as a Blend

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/extra/metalness/metalnessAsBlend.png" alt="" width="400"/><br><em>En este material el hierro tiene una metalidad de 1, mientras que el óxido tiene una metalidad de 0. Puede haber valores intermedios de metalidad donde el óxido pasa a la plancha.</em></td>
    <td style="border: 0;" valign="top">Si bien el valor de metalness suele ser 0 o 1 (es decir, totalmente no metálico o totalmente metálico), los valores intermedios son significativos. Estos valores representan superficies en las que materiales metálicos y no metálicos se mezclan a pequeña escala, en casos como pinturas que contienen partículas o escamas metálicas. Además, como se ha mencionado anteriormente, los materiales de OpenPBR se crean a partir de capas que representan interfaces físicas distintas. Es totalmente posible que la capa base de un material (es la capa "core") sea metálica, pero para que tenga una capa de capa no metálica por encima - la capa de capa no es simplemente un control de specular adicional - representa una superficie física separada a través de la cual la luz debe pasar. Este sería el caso con algunos tipos de pintura de coches, por ejemplo: las escamas metálicas se representarían en la capa Base del material, mientras que la capa Coat representaría una capa transparente.</td>
  </tr>
</table>

### Combinación de capas para crear comportamientos complejos

Los materiales complejos, como el vidrio esmerilado o la pintura de coches mencionados anteriormente en esta sección, se crean combinando varios comportamientos de forma controlada. Por ejemplo:

* **Vidrio congelado**: transmisión combinada con alta rugosidad y dispersión
* **Metal pintado**: una superficie dieléctrica sobre una base metálica, a menudo con una capa clara En lugar de pensar en términos de ajustes preestablecidos, es más eficaz considerar qué comportamientos físicos están presentes y cómo interactúan. Los materiales de OpenPBR se definen mediante componentes físicamente significativos que describen la forma en que la luz interactúa con las superficies. Los &#39;tipos&#39; materiales surgen naturalmente de combinaciones de comportamientos, en lugar de ser seleccionados explícitamente. Al centrarse en la interacción con la luz, la fusión y las capas, los artistas pueden crear una amplia gama de materiales realistas al tiempo que mantienen la verosimilitud física.

## Trabajo con OpenPBR

### La arquitectura conceptual de un material de OpenPBR

OpenPBR está diseñado como un modelo único de sombreado de superficie unificado capaz de representar una amplia gama de materiales del mundo real. En lugar de cambiar entre sombreadores diferentes para diferentes tipos de materiales, OpenPBR combina varias características de superficie en una sola arquitectura en capas.

Conceptualmente, se puede pensar en un material de OpenPBR como poseedor de tres elementos clave:

* **Marco de trabajo básico**: El OpenPBR considera que un material está hecho de bloques de construcción físicos que se pueden mezclar (mezcla horizontal) o apilar uno encima del otro (capa vertical). Esos bloques pueden reaccionar a la luz de manera diferente. Cuando se fusionan dos de estos bloques, el resultado será una fusión del reflejo de los dos. Sin embargo, cuando se colocan en capas, el bloque más bajo solo recibirá y reflejará tanta luz como permita el bloque más alto. Esta configuración permite a los artistas considerar el material como una mezcla de componentes más sencillos. La definición de esos componentes y su ubicación es el segundo elemento clave:
* **Serie de capas que contribuyen al marco de trabajo compartido**: Cada material tendrá una capa base, que determina características como el color principal del material, o si el material es rugoso o liso. Los materiales también pueden tener capas adicionales (película fina, capa y zumbido) que pueden reproducir efectos como barniz o dust.
* **Un conjunto de controles orientados al artista**: una interfaz que permite a un artista controlar las reglas del marco de reflexión, y por lo tanto, la apariencia del material de OpenPBR en general. En función de cómo el software específico pueda representar estos controles en su interfaz de usuario, se trata básicamente de un conjunto de controles o controles deslizantes que permiten a un artista controlar, por ejemplo, qué tan fuertes deben ser los reflejos o qué matiz de color debe aparecer en determinados ángulos de visualización. Algunos controles se aplicarán al marco general (y, por lo tanto, se aplicarán a todas las capas del material); algunos controles solo se aplicarán a capas específicas.

### Capas de materiales dentro del marco

![](../assets/openpbrf/model_schematic2.png) Haga clic para hacer zoom. *Figura adaptada de la especificación OpenPBR Surface, © Academy Software Foundation, usada bajo la licencia Apache 2.0*

Cada capa aporta un efecto físico específico y el modelo de material gestiona la forma en que interactúan de forma físicamente plausible. Esta estructura en capas es coherente entre las implementaciones de OpenPBR. Las aplicaciones individuales siguen siendo libres de presentar una interfaz de usuario que controle estas capas como mejor les parezca.

>[!NOTE]
>
> Hay dos &quot;capas&quot; que no aparecen en el diagrama anterior:
>
> * **Specular**: Controla lo brillante o reflectante que es una superficie, tanto si la base es metálica como si no. El specular existe dentro de la pila de capas, pero no es en sí mismo una capa real, sino una propiedad de las capas base y de capa que sí aparecen en la pila de capas.
> * **Geometría**: Mientras que otras capas de OpenPBR determinan de qué está hecho el material, la capa Geometría define la forma y la presencia a las que se aplica el material, incluida la opacidad, las normales, las tangentes y el comportamiento de las paredes delgadas.
>
> Continuaremos refiriéndonos a la Geometría y el Specular como &quot;capas&quot; para simplificar.

Las capas que constituyen una superficie de OpenPBR, desde lo más profundo hasta lo más exterior, son:

* **La capa base**: En la parte inferior de un material de OpenPBR, la capa Base define la interacción fundamental entre la luz y el material. Los parámetros de esta capa Base determinan el color principal del material, si es rugoso o liso, y si (en términos de cómo interactúa con la luz) es metálico o no metálico (también conocido como dieléctrico).

>[!NOTE]
>
> Para la mayoría de los materiales la capa Base es absolutamente necesaria. Las capas superiores (película fina, capa y pelusa) pueden estar presentes o no, dependiendo del tipo de material que se esté reproduciendo en 3D.

* **Película fina**: Si existe, se coloca una capa de película fina sobre la capa base. Reproduce la apariencia visual de capas superficiales muy finas, produciendo colores iridiscentes, como los que se ven en burbujas de jabón, metal quemado o películas de aceite.

* **Abrigo**: Una capa de capa, si existe, reproduce una capa transparente y reflectante colocada sobre cualquier otra capa, excepto Fuzz. Esto puede simular efectos reales como barnices, superficies húmedas o ciertos tipos de pintura de coches.

* **Fuzz**: Si está presente, una capa de Fuzz reproduce el reflejo a partir de microfibras. Se puede utilizar para reproducir la apariencia de una tela difusa, por ejemplo, o una capa de dust.

La forma en que cada una de estas capas interactúa con la luz viene determinada por un conjunto de parámetros.

### Tipos de materiales

El Metalness Base, a su vez, determina las características que se aplican a la siguiente capa del material - un material completamente no metálico posee características diferentes a un material metálico.

#### Materiales no metálicos (Base Metalness = 0)

Un material totalmente no metálico (es decir, un material con un valor de Metalness base de 0) se clasificará en tres tipos básicos: **difuso**, **subsuperficial** o **translúcido**. Tenga en cuenta que los materiales no se incluyen necesariamente en uno solo de los tipos de base anteriores. Materiales más complejos que son una mezcla de estos tipos de materiales básicos son posibles.

Los **materiales difusos** suelen ser materiales opacos, como la madera o la piedra.

**Materiales subterráneos** dispersión la luz internamente; la piel o la cera quedarían comprendidas en este tipo de material, por ejemplo.

Los **materiales base translúcidos** permiten que la luz los atraviese; estos incluyen materiales como el vidrio, el cristal o ciertos líquidos. Los parámetros clave que se deben tener en cuenta son los parámetros globales de specular, los parámetros de la capa base y los parámetros específicos de transmisión que se indican a continuación. La diferencia entre la dispersión subsuperficial (SSS) y la transmisión es esencialmente que el SSS no permite ver a través del material: un haz de luz se dispersa dentro de un material y luego vuelve a salir por el mismo lado. La transmisión, a la inversa, rige los materiales que son al menos parcialmente transparentes: un rayo de luz pasa a través del material.

#### Materiales metálicos (metalidad > 0)

Por el contrario, cuando se activa Metalness Base (es decir, tiene un valor mayor que 0), adquiere algunas características de comportamiento específicas:

* El valor Color de Specular del material controla el matiz del material cerca de los ángulos de pastoreo (cuando la luz golpea una superficie en un ángulo cercano al paralelo).
* El valor de color base del material controla el reflejo con una incidencia normal (es decir, cuando la luz se refleja a 90 grados de la superficie).
* El valor de Peso del Specular del material escala la fuerza general de los reflejos, afectando a los ángulos normales y de pastoreo.

Combinados con los siguientes canales, los materiales metálicos pueden crear diversos efectos.

**Emisión**

La emisión permite que una superficie actúe como fuente de luz emitiendo luz directamente. Si bien la emisión no es un fenómeno reflexivo, se incluye dentro del modelo de material del OpenPBR de manera que los materiales emisores puedan definirse de manera coherente junto con las propiedades reflexivas y transmisivas.

**Película fina**

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/thin-film/ior/thinFIlmIOR15.png" alt=""/></td>
    <td style="border: 0;" valign="top">Un efecto de película fina, si existe, reproduce la apariencia visual de las capas superficiales muy finas, produciendo colores iridiscentes, como los que se ven en las burbujas de jabón o las películas de aceite.</td>
  </tr>
</table>

**Abrigo**

Una capa de capa, si existe, reproduce una capa transparente y reflectante colocada sobre cualquier otra capa, excepto Fuzz. Esto puede simular efectos del mundo real como el barniz o ciertos tipos de pintura de coches. Una capa Coat se define por un rango entre 0 y 1; si se establece este valor en 0, se desactiva por completo la capa Capa.

**Fuzz**

Se puede añadir una capa Fuzz para reproducir el aspecto de superficies similares a una tela, como terciopelo o satén, o se puede utilizar para crear el efecto de una capa de dust en una superficie.

### Conceptos de flujo de trabajo de material

#### Pensar en comportamientos de luz, no en etiquetas materiales

El OpenPBR se diseña en función de cómo se comporta la luz, en lugar de alrededor de categorías de materiales fijas. En lugar de seleccionar un sombreado que represente &quot;vidrio&quot;, &quot;piel&quot; o &quot;metal&quot;, los artistas construyen materiales describiendo cómo la luz se refleja desde una superficie, pasa a través de ella, dispersiones dentro de ella o es emitida por ella. Este enfoque fomenta un cambio de mentalidad: los materiales no son tipos predefinidos, sino combinaciones de comportamientos físicos. Un único material del mundo real puede implicar varios de estos comportamientos a la vez, y el OpenPBR hace que esos aportes sean explícitos en lugar de ocultarlos detrás de ajustes preestablecidos o modelos de sombreado opacos.

#### Separación de preocupaciones: Los materiales son independientes de la iluminación

Un principio básico de los flujos de trabajo basados en la física es la separación de la descripción del material de la iluminación. Los materiales se crean para describir las propiedades intrínsecas de superficie y volumen, mientras que la iluminación define el entorno en el que se revelan esas propiedades. Esta separación reduce la interdependencia y hace que las escenas complejas sean más manejables. Un material de OpenPBR bien creado debe seguir siendo creíble en una amplia gama de condiciones de iluminación, sin requerir ajustes específicos de la escena. A menor escala, el OpenPBR continúa con esta filosofía manteniendo los parámetros lo más independientes posible, permitiendo a los artistas ajustar un aspecto de un material sin desestabilizar a los demás de forma involuntaria.

#### Materiales de construcción incrementales

El OpenPBR fomenta un enfoque gradual de la creación de materiales. La mayoría de los flujos de trabajo empiezan estableciendo la respuesta de la superficie (cómo se refleja la luz del objeto) antes de introducir efectos de volumen como la transmisión o la dispersión subsuperficial. Los comportamientos secundarios, incluidas las interferencias de pelusa, emisión o película fina, se suelen colocar en capas más adelante para perfeccionar el realismo o lograr indicaciones visuales específicas. Este enfoque por capas ayuda a los artistas a diagnosticar los problemas con más facilidad y evitar complicar demasiado los materiales al principio del proceso. Al pasar de comportamientos principales a secundarios, los materiales siguen siendo más fáciles de comprender, depurar y reutilizar.

#### Ajustes preestablecidos y ejemplos como herramientas de aprendizaje

El OpenPBR incluye ajustes preestablecidos para los materiales comunes, pero estos se entienden mejor como ejemplos de referencia en lugar de soluciones finales. El examen de cómo los ajustes preestablecidos equilibran parámetros como la rugosidad, el metal o la profundidad de transmisión puede ayudar a los artistas a comprender cómo se construyen los resultados visuales específicos. En lugar de confiar en los ajustes preestablecidos al por mayor, los flujos de trabajo de OpenPBR animan a los artistas a observar materiales del mundo real, identificar los comportamientos de luz subyacentes en juego y recrear esos comportamientos mediante controles físicamente significativos.

## Canales de OpenPBR y parámetros

### Especular

![](../assets/openpbrf/renders/specular/color/specColorYellowNoMetal.png){width="250"}

*Material gris dieléctrico (no metálico) con color amarillo de specular.*

+++parámetros de specular

**Peso del Specular**

Mientras que el color del Specular determina el matiz de color de cualquier reflejo en los ángulos de pastoreo, el peso del Specular determina la intensidad de dichos reflejos, entre un rango de 0 a 1. Con un valor de 0, no hay ningún reflejo en los ángulos de pastoreo; a valores más altos, la intensidad de tales reflexiones se hace más pronunciada. Ten en cuenta que, en el &quot;mundo real&quot;, cada material es reflectante en cierto grado, y si se recreara en 3D tendría un valor de Peso del Specular mayor que 0. Téngase en cuenta también que el peso del Specular no debe considerarse en modo alguno un valor &quot;primario&quot; para parametrizar el reflejo de un material; La rugosidad del specular (véase a continuación) es siempre una consideración clave para determinar la reflectividad de un material.

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/weight/weight0.png" alt=""/><br><em>Peso del specular = 0,0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/weight/weight05.png" alt=""/><br><em>Peso del specular = 0,5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/weight/weight1.png" alt=""/><br><em>Peso del specular = 1,0</em></td>
  </tr>
</table>

**Color de Specular**

Esto determina cualquier matiz de color que se refleje cuando la luz se refleja en un ángulo de pastoreo (un ángulo casi paralelo a la superficie de un material). En el caso de los materiales metálicos (véase Metalness, más adelante), puede aplicarse un matiz de color; para materiales no metálicos, el color del Specular debe ser, por lo general, blanco. Las imágenes a continuación muestran diferentes colores de specular en materiales metálicos y no metálicos.

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/color/specColorGreen.png" alt=""/><br></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/color/specColorViolet.png" alt=""/><br></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/color/specColorYellow.png" alt=""/><br></td>
  </tr>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/color/specColorGreenNoMetal.png" alt=""/><br><em>Color verde del Specular</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/color/specColorPurpleNoMetal.png" alt=""/><br><em>Color Specular violeta</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/color/specColorYellowNoMetal.png" alt=""/><br><em>Color amarillo del Specular</em></td>
  </tr>
</table>

**Rugosidad del Specular**

Al igual que el parámetro Rugosidad en un material PBR, Rugosidad del Specular en un material de OpenPBR representa una variación microscópica de la superficie: incluso las superficies que parecen lisas a simple vista poseen pequeñas imperfecciones que dispersión la luz reflejada. Este valor reproduce ese efecto, controlando la suavidad o rugosidad de una superficie en sus reflejos mediante la definición de la nitidez o amplitud del reflejo de la luz. Los materiales con una rugosidad baja producirán reflejos afilados, similares a los de un espejo. Por el contrario, los materiales con una alta rugosidad producirán reflejos suaves y desenfocados.

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/roughness/roughness01.png" alt=""/><br><em>Rugosidad del specular = 0,1</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/roughness/roughness05.png" alt=""/><br><em>Rugosidad del specular = 0,5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/roughness/roughness08.png" alt=""/><br><em>Rugosidad del specular = 0,8</em></td>
  </tr>
</table>

Tenga en cuenta que esto no tiene ninguna relación con la cantidad general de luz reflejada: es simplemente una medida de si esa luz se refleja de una manera muy enfocada o difusa.

**IOR (Índice de refracción)**

El IOR describe la intensidad con la que un material interactúa con la luz, controlando tanto la forma en que los rayos de luz se doblan (se refractan) al entrar en el material, como su aspecto reflectante, en particular en ángulos de visión poco profundos (rasgados). Las superficies menos reflectantes, como el agua o algunos plásticos, tendrán un IOR bajo. Superficies más reflectantes - vidrio, o algunas gemas, por ejemplo - tendrán un mayor IOR y un efecto de refracción más fuerte. El IOR de un material es un valor físico, y como tal es un número objetivo, más que una cuestión de interpretación artística. Al crear un material determinado, solo tiene que buscar el IOR del material y asegurarse de que esté configurado correctamente para garantizar que el material reacciona correctamente con la luz. Una serie de fuentes están disponibles en línea listando los IORs de diversos materiales. Por ejemplo, el IOR de granito es 1,43; si se está creando un material de granito, se introduce este valor como IOR, lo que garantiza que la luz refleje el material de forma realista. Tenga en cuenta que el IOR no afecta a los materiales metálicos (consulte Metalness, más adelante). El cambio del valor IOR de un material metálico no afectará a su aspecto.

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/ior/IOR1.png" alt=""/><br><em>IOR = 1,1</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/ior/IOR15.png" alt=""/><br><em>IOR = 1,5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/ior/IOR2.png" alt=""/><br><em>IOR = 2,0</em></td>
  </tr>
</table>

**Anisotropía**

Cuando las variaciones de la superficie microscópica están algo alineadas en la misma dirección, como las ranuras, el reflejo del material tenderá a depender de la dirección de visualización y se estirará perpendicularmente a las ranuras. Cuanto más alineadas estén esas ranuras, más pronunciado será el efecto. El valor de Anisotropía del material define si los reflejos de una superficie aparecen igual en todas las direcciones o si se extienden de una forma determinada. Esto podría reproducir el efecto de materiales como el metal cepillado, por ejemplo, donde los reflejos a lo largo del &quot;efecto pincel&quot; son mucho más largos. El reflejo anisotrópico también puede producirse de formas más sutiles cuando una superficie pulida se mancha con una huella dactilar o cuando se estira una superficie deformable, como la piel seca.

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/anisotropy/anisotropy0.png" alt=""/><br><em>Anisotropía = 0,0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/anisotropy/anisotropy05.png" alt=""/><br><em>Peso de la anisotropía = 0,5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/anisotropy/anisotropy1.png" alt=""/><br><em>Peso de la anisotropía = 1,0</em></td>
  </tr>
</table>

**Tangente de Anisotropía**

Cuando existe algún grado de Anisotropía (es decir, el valor de Anisotropía del material es mayor que 0), la Tangente de Anisotropía indica la dirección dominante de las ranuras. El reflejo se extenderá perpendicularmente a esa dirección.

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/tangent/tangentGreen.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/tangent/tangentOrange.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/specular/tangent/tangentRed.png" alt=""/></td>
  </tr>
</table>

*Diferentes orientaciones de tangente de Anisotropía.*

+++

### Geometría

El OpenPBR también incluye parámetros que afectan a la forma en que el material interactúa con la geometría, como la opacidad y el comportamiento de paredes delgadas. Estos controles determinan si una superficie debe tratarse como si tuviera thickness físico o como una capa fina, lo que es particularmente importante para materiales como el papel, las hojas, las ventanas o la tela

+++Parámetros de geometría

* **Pared fina**: Con las paredes delgadas activadas, el material se considera microscópicamente delgado. Se considera que la luz atraviesa el material sin refracción visible.
* **Opacidad**: Determina si es posible ver parcial o totalmente a través de un material. Tenga en cuenta que, mientras que el parámetro Transmisión define la transparencia de un material, el parámetro Opacidad se puede utilizar para definir el neteo, es decir, esencialmente &quot;eliminar&quot; la información de material para crear taladros.

+++

### La capa base

En la parte inferior del modelo de OpenPBR, la capa Base representa la interacción fundamental entre la luz y el material de superficie en sí. La capa base se define mediante cuatro características: Peso base, Color base, Metalness y Rugosidad difusa.

<table>
  <tr style="border: 0;">
    <th style="border: 0;"><img src="../assets/openpbrf/renders/base/basecolor/baseColorYellow.png" alt=""/></th>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/metalness/metalness1Colored.png" alt=""/></td>
  </tr>
</table>

*Materiales dieléctricos y metálicos amarillos, uno al lado del otro.*

+++Características de la capa base

* **Peso base**: Básicamente define la intensidad del color base (véase a continuación), en una escala de 0 a 1, con un valor de 0 que da como resultado un material principalmente negro (sin color) y un valor de 1 (una combinación de la mayor cantidad posible de luz roja, verde y azul).

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/weight/baseWeight0.png" alt=""/><br><em>Peso base = 0,0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/weight/baseWeight05.png" alt=""/><br><em>Peso base = 0,5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/weight/baseWeight1.png" alt=""/><br><em>Peso base = 1,0</em></td>
  </tr>
</table>

* **Color base**: Esto determina el &#39;color principal&#39; de un material, estableciendo el albedo -es decir, la cantidad de luz roja, verde y azul reflejada- tanto de las bases metálicas como difusas (para las no metálicas). Como se ha indicado anteriormente, mientras que el color base determina los colores que se reflejan, el ajuste Grosor base determina la intensidad de este reflejo.

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/basecolor/baseColorGreen.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/basecolor/baseColorViolet.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/basecolor/baseColorYellow.png" alt=""/></td>
  </tr>
</table>

* **Metalness**: Define si un material se comporta como no metálico (dieléctrico) o metálico, en una escala de 0 a 1 (0 = dieléctrico, 1 = totalmente metálico y opaco).

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/metalness/metalness05.png" alt=""/><br><em>Metalness = 0,5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/metalness/metalness1.png" alt=""/><br><em>Metalness= 1,0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/metalness/metalness1Colored.png" alt=""/><br><em>Metalness = 1.0 con color base amarillo</em></td>
  </tr>
</table>

* **Rugosidad de difusión**: Define la rugosidad de la micro superficie de un material, que va desde 0 (que posee un reflejo muy suave y uniforme) hasta 1 (con un reflejo muy áspero y difuso), adecuado para materiales como roca o corteza de árbol.

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/diffuse-rough/diffuseRoughness0.png" alt=""/><br><em>Rugosidad difusa = 0,0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/diffuse-rough/diffuseRoughness1.png" alt=""/><br><em>Rugosidad difusa = 1,0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/base/diffuse-rough/diffuseRoughnessSplit.png" alt=""/><br><em>En paralelo de 0,0 frente a 1,0</em></td>
  </tr>
</table>

+++

### Subsuperficie

![](../assets/openpbrf/renders/sss/radius/SSSRadius10_vers2.png){width="250"}

*Material que utiliza el canal subsuperficial. Observe la translucidez presente en las manos y otras áreas delgadas de la malla.*

+++Parámetros de subsuperficie

* **Peso subsuperficial**: Esto define la cantidad de dispersión subsuperficial que se utiliza, esencialmente, la cantidad de luz que entra en el material.

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/sss/weight/TransmissionWeight0.png" alt=""/><br><em>Peso = 0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/sss/weight/SSSWeight05.png" alt=""/><br><em>Peso = 0,5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/sss/weight/SSSWeight1.png" alt=""/><br><em>Peso = 1,0</em></td>
  </tr>
</table>

* **Color de subsuperficie**: Define el color general de cualquier luz que resurge desde debajo de la superficie de un material. Los colores más claros suelen dar como resultado una dispersión más brillante y visible; un valor de negro no produce ningún efecto de dispersión subsuperficial.

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/sss/color/SSSColorGreen.png" alt=""/></td>
    <td><img src="../assets/openpbrf/renders/sss/color/SSSColorPurple.png" alt=""/></td>
    <td><img src="../assets/openpbrf/renders/sss/color/SSSColorYellow.png" alt=""/></td>
  </tr>
</table>

* **Radio subsuperficial**: Define hasta dónde puede viajar la luz dentro de un material antes de dispersarse o absorberse. Con un valor bajo, la luz solo recorrerá una corta distancia; como resultado, los materiales tendrán un aspecto denso. Con un radio alto, la luz viaja más lejos; los materiales tendrán un aspecto suave, ceroso y translúcido.

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/sss/radius/SSSRadius1_vers2.png" alt=""/><br><em>Radio = 1</em></td>
    <td><img src="../assets/openpbrf/renders/sss/radius/SSSRadius10_vers2.png" alt=""/><br><em>Radio = 10</em></td>
    <td><img src="../assets/openpbrf/renders/sss/radius/SSSRadius20_vers2.png" alt=""/><br><em>Radio = 20</em></td>
  </tr>
</table>

* **Escala de radio subsuperficial**: Controla la dependencia del canal de color del trazado libre medio. En otras palabras, hasta dónde viaja la luz a través del material de forma independiente por canal del RGB antes de ser absorbida o dispersada. Esto produce la variación de color característica que se observa en los materiales subsuperficiales: en las áreas más delgadas de la malla, donde la luz se desplaza a una distancia más corta, el color cambia hacia el canal que tenga el radio más largo.\\

El valor predeterminado (1, 0.5, 0.25) significa que la luz roja viaja más profundamente, seguida por el verde y luego el azul, que coincide estrechamente con el comportamiento de muchos materiales subsuperficiales del mundo real, incluida la piel.

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/sss/radiusScale/radiusScaleDefault.png" alt=""/><br><em>Escala de radio = predeterminada</em></td>
    <td><img src="../assets/openpbrf/renders/sss/radiusScale/radiusScaleGrey.png" alt=""/><br><em>Escala de radio = Gris</em></td>
    <td><img src="../assets/openpbrf/renders/sss/radiusScale/radiusScaleWhite.png" alt=""/><br><em>Escala de radio = Blanco</em></td>
    <td><img src="../assets/openpbrf/renders/sss/radiusScale/radiusScaleYellow.png" alt=""/><br><em>Escala de radio = Amarillo</em></td>
    <td><img src="../assets/openpbrf/renders/sss/radiusScale/radiusScaleBrown.png" alt=""/><br><em>Escala de radio = Marrón</em></td>
  </tr>
</table>

* **Anisotropía subsuperficial**: Define la dirección en la que la luz prefiere la dispersión dentro de un material subsuperficial. Con un valor de 0, la luz se dispersión uniformemente en todas las direcciones. Con un valor positivo, la luz tenderá a la dispersión hacia adelante, en la misma dirección que el rayo de luz inicial; esto normalmente dará como resultado que los materiales tengan un aspecto más claro y traslúcido. Con un valor negativo, la luz tenderá a la dispersión hacia atrás hacia la fuente del haz de luz; esto normalmente dará a los materiales un aspecto más opaco y denso.

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/sss/anisotropy/SSSanisotropy-1.png" alt=""/><br><em>Anisotropía = -1</em></td>
    <td><img src="../assets/openpbrf/renders/sss/anisotropy/SSSanisotropy0.png" alt=""/><br><em>ANISOTROPÍA = 0</em></td>
    <td><img src="../assets/openpbrf/renders/sss/anisotropy/SSSanisotropy1.png" alt=""/><br><em>ANISOTROPÍA = 1</em></td>
  </tr>
</table>

+++

### Transmisión

La transmisión controla la cantidad de luz que puede atravesar un material. A diferencia de Subsuperficie, la transmisión controla la cantidad de luz que pasa por el objeto por completo, mientras que la subsuperficie controla la cantidad de luz que se refleja desde el interior del objeto hasta la superficie.

![](../assets/openpbrf/renders/transmission/color/transmission_orange.png){width="250"}

*Ejemplo de un material altamente transmisivo con un color de transmisión naranja.*

+++Parámetros de transmisión

* **Peso**: Controla la cantidad de luz que puede pasar a través de la superficie del material. A menudo se usa para materiales transparentes como líquidos o vidrio.

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/weight/TransmissionWeight0.png" alt=""/><br><em>Peso = 0,0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/weight/TransmissionWeight05.png" alt=""/><br><em>Peso = 0,5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/weight/TransmissionWeight1.png" alt=""/><br><em>Peso = 1,0</em></td>
  </tr>
</table>

* **Color**: Determina el color de la luz que pasa por un material.

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/color/transmission_green.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/color/transmission_orange.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/color/transmission_purple.png" alt=""/></td>
  </tr>
</table>

* **Profundidad**: Define, en centímetros, hasta dónde debe viajar un rayo de luz por un material antes de que el color de transmisión alcance la saturación completa; en esencia, la rapidez con la que la luz capta el color cuando pasa por un material transparente (o parcialmente transparente). Para materiales con baja Profundidad de transmisión, la luz captará el color muy rápidamente, lo que significa que incluso las partes muy delgadas del material se ven muy coloreadas. Por el contrario, con una alta profundidad, las secciones más gruesas se verán muy oscuras o casi opacas, y el material tendrá una apariencia &#39;densa&#39;, como resina de color o líquido grueso.

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/depth/transmissionDepth0.png" alt=""/><br><em>PROFUNDIDAD = 0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/depth/transmissionDepth1.png" alt=""/><br><em>PROFUNDIDAD = 1</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/depth/transmissionDepth10.png" alt=""/><br><em>Profundidad= 10</em></td>
  </tr>
</table>

* **Color de Dispersión**: Esto define el color y la intensidad de la luz dispersada dentro de un material transparente o parcialmente transparente. Básicamente define la &#39;nubosidad&#39; interna de un material, determinando cómo se extiende y se suaviza la luz dentro del material. Color de dispersión es útil para reproducir materiales donde la luz no viaja limpiamente o en línea recta, como, por ejemplo, ciertos plásticos, leche o zumo de manzana turbio, o incluso para grandes masas de agua (creando el matiz azul del océano, por ejemplo).

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/scatter/transmissionScatterDarkGrey.png" alt=""/><br><em>Color de dispersión gris oscuro</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/scatter/transmissionScatterMiddleGrey.png" alt=""/><br><em>Color de dispersión gris medio</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/scatter/transmissionScatterWhite.png" alt=""/><br><em>Color de dispersión blanca</em></td>
  </tr>
</table>

* **Anisotropía de Dispersión**: Esto determina qué dirección tenderá la luz a la dispersión dentro de un material. Con un valor de 0, la luz se dispersión uniformemente en todas las direcciones. Con un valor positivo, la luz tenderá a la dispersión hacia adelante, en la misma dirección que el rayo de luz inicial; esto normalmente dará como resultado que los materiales tengan un aspecto más claro y más parecido al cristal. Con un valor negativo, la luz tenderá a la dispersión hacia atrás hacia la fuente del haz de luz; esto normalmente dará a los materiales un aspecto más escarchado o calcáreo.

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/anisotropy/transmissionAnisotropy-1.png" alt=""/><br><em>Anisotropía = -1</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/anisotropy/transmissionAnisotropy0.png" alt=""/><br><em>ANISOTROPÍA = 0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/anisotropy/transmissionAnisotropy1.png" alt=""/><br><em>ANISOTROPÍA = 1</em></td>
  </tr>
</table>

>[!NOTE]
>
> La Anisotropía de la dispersión depende de la dirección de la luz, por lo que el resultado de esta dispersión cambiará dependiendo de dónde se coloque la fuente de luz, en relación con el material que se ilumine.

* **Dispersión (Abbe)**: Esto define la cantidad de colores diferentes de la luz que se doblan al pasar por un material transparente, lo que resulta en una división del color, halos similares al arco iris o bordes de color en luz refractada. Un valor de dispersión (Abbe) de 0 desactiva este efecto por completo. Un valor bajo de Dispersión (Abbe) dará como resultado una separación de colores muy visible (como puede verse en un prisma), mientras que un valor alto de Dispersión (Abbe) dará como resultado una separación de colores débil o insignificante y una refracción más limpia y clara en general. (El parámetro Dispersión (Abbe) recibe el nombre de Ernst Abbe, físico e ingeniero óptico del siglo XIX.)

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/abbe/transmissionAbbe20.png" alt=""/><br><em>Abbe = 20</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/abbe/transmissionAbbe45.png" alt=""/><br><em>Abbe = 45</em></td>
  </tr>
</table>

* **Dispersión de transmisión**: Al igual que con los parámetros de Peso en otros lugares, este valor define la intensidad de la dispersión de luz dentro del material. Esto es más evidente en los bordes de las refracciones de alto contraste.

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/dispersion/transmissionDispersionScale0.png" alt=""/><br><em>Dispersión de la transmisión = 0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/dispersion/transmissionDispersionScale05.png" alt=""/><br><em>Dispersión de la transmisión = 0,5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/transmission/dispersion/transmissionDispersionScale1.png" alt=""/><br><em>Dispersión de la transmisión = 1,0</em></td>
  </tr>
</table>

+++

### Emisión

Emisión controla si el material emite o no su propia luz (independientemente de la luz reflejada) y te permite establecer el color y la intensidad de la luz emitida.

![](../assets/openpbrf/renders/emission/color/emissionColorGreen.png){width="250"}

*Material de emisión verde brillante.*

+++Parámetros de emisión

* **Luminancia**: Define el brillo de la luz emitida por el material, medida en cd/m², también conocido como nits. Esta medida presume de luz blanca; cambiar el color de la luz (véase a continuación) puede afectar al brillo general.

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/emission/luminance/emissionLuminance100.png" alt=""/><br><em>Luminancia = 100</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/emission/luminance/emissionLuminance400.png" alt=""/><br><em>Luminancia = 400</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/emission/luminance/emissionLuminance1000.png" alt=""/><br><em>Luminancia = 1000</em></td>
  </tr>
</table>

* **Color**: Determina el color de luz emitido por el material.

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/emission/color/emissionColorGreen.png" alt=""/></td>
    <td><img src="../assets/openpbrf/renders/emission/color/emissionColorPurple.png" alt=""/></td>
    <td><img src="../assets/openpbrf/renders/emission/color/emissionColorYellow.png" alt=""/></td>
  </tr>
</table>

+++

### Película fina

![](../assets/openpbrf/renders/thin-film/thickness/thinFilmThickness05.png){width="250"}

*material base oscuro con una capa de película fina.*

+++Parámetros de película fina

* **Peso**: Al igual que con otros parámetros de Grosor, esto controla la intensidad del efecto de película fina, con un valor entre 0 y 1. Casi 0 efectos de película fina son apenas visibles; en el extremo superior de este rango son mucho más pronunciadas.

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/thin-film/weight/thinFilmWeight0.png" alt=""/><br><em>Peso = 0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/thin-film/weight/thinFilmWeight05.png" alt=""/><br><em>Peso = 0,5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/thin-film/weight/thinFilmWeight1.png" alt=""/><br><em>Peso = 1,0</em></td>
  </tr>
</table>

* **Thickness**: Define el thickness de la capa de película, en micrómetros. En un material físicamente preciso, la mayoría de los efectos de película fina se producen a un thickness de entre 0 y 1 micrómetro.

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/thin-film/thickness/thinFilmThickness0.png" alt=""/><br><em>THICKNESS = 0</em></td>
    <td><img src="../assets/openpbrf/renders/thin-film/thickness/thinFilmThickness05.png" alt=""/><br><em>Thickness = 0,5</em></td>
    <td><img src="../assets/openpbrf/renders/thin-film/thickness/thinFilmThickness1.png" alt=""/><br><em>Thickness = 1,0</em></td>
  </tr>
</table>

* **Índice de refracción (IOR)**: Como se ha indicado anteriormente, el IOR de un material determina la intensidad con la que reacciona un material con la luz. La capa de película fina de un material de OpenPBR tiene su propio IOR. Por ejemplo, el diamante tiene un IOR de 2,417.

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/thin-film/ior/thinFIlmIOR1.png" alt=""/><br><em>IOR = 1</em></td>
    <td><img src="../assets/openpbrf/renders/thin-film/ior/thinFIlmIOR15.png" alt=""/><br><em>IOR = 1,5</em></td>
    <td><img src="../assets/openpbrf/renders/thin-film/ior/thinFIlmIOR2.png" alt=""/><br><em>IOR = 2</em></td>
  </tr>
</table>

+++

### Capa

![](../assets/openpbrf/renders/coat/color/coatColorPurple.png){width="250"}

*Capa de capa púrpura de baja rugosidad.*

+++Parámetros de capa

* Peso: Básicamente determina la intensidad de la capa de capa de capa. Si se establece este valor en un valor mínimo de 0, se deshabilita por completo el Escudo. los valores más altos aumentan la intensidad de la capa.

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/coat/weight/coatWeight0.png" alt=""/><br><em>Peso = 0</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/coat/weight/coatWeight05.png" alt=""/><br><em>Peso = 0,5</em></td>
    <td style="border: 0;" valign="top"><img src="../assets/openpbrf/renders/coat/weight/coatWeight1.png" alt=""/><br><em>Peso = 1,0</em></td>
  </tr>
</table>

* Color: Determina el color general de la capa Capa, que puede teñir el reflejo de la capa Base que se encuentra debajo.

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/coat/color/coatColorGreen.png" alt=""/></td>
    <td><img src="../assets/openpbrf/renders/coat/color/coatColorPurple.png" alt=""/></td>
    <td><img src="../assets/openpbrf/renders/coat/color/coatColorYellow.png" alt=""/></td>
  </tr>
</table>

* Oscurecimiento: Determina el grado de oscurecimiento y saturación del reflejo de la capa Base. Por ejemplo, la madera barnizada suele aparecer más oscura que la misma madera si no está barnizada; la característica Oscurecimiento puede reproducir este efecto.

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/coat/darkening/coatDarkening0.png" alt=""/><br><em>Oscurecimiento = 0</em></td>
    <td><img src="../assets/openpbrf/renders/coat/darkening/coatDarkening05.png" alt=""/><br><em>Oscurecimiento = 0,5</em></td>
    <td><img src="../assets/openpbrf/renders/coat/darkening/coatDarkening1.png" alt=""/><br><em>Oscurecimiento = 1,0</em></td>
  </tr>
</table>

* Índice de refracción (IOR): Básicamente, una definición numérica de cómo reflectante aparece una superficie no metálica, basada en cómo se comporta la luz dentro de la capa Coat.

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/coat/ior/coatIOR14.png" alt=""/><br><em>IOR = 1,4</em></td>
    <td><img src="../assets/openpbrf/renders/coat/ior/coatIOR2.png" alt=""/><br><em>IOR = 2</em></td>
    <td><img src="../assets/openpbrf/renders/coat/ior/coatIOR3.png" alt=""/><br><em>IOR = 3</em></td>
  </tr>
</table>

* Rugosidad: Como se ha mencionado al comentar la capa Base, la rugosidad de la superficie define qué tan reflectante es una superficie: las superficies lisas reflejan la luz de manera muy uniforme, mientras que las superficies rugosas dispersiones la luz en direcciones aleatorias. Una capa de capa tendrá su propio grado de rugosidad.

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/coat/roughness/coatRoughness01.png" alt=""/><br><em>Rugosidad = 0,1</em></td>
    <td><img src="../assets/openpbrf/renders/coat/roughness/coatRoughness05.png" alt=""/><br><em>Rugosidad = 0,5</em></td>
    <td><img src="../assets/openpbrf/renders/coat/roughness/coatRoughness08.png" alt=""/><br><em>Rugosidad = 0,8</em></td>
  </tr>
</table>

>[!NOTE]
>
> Tenga en cuenta que, incluso si una capa Base es suave (es decir, su valor de Rugosidad es cercano a 0), la Rugosidad de la capa Coat puede hacer que el material general parezca mucho más rugoso.

* Anisotropía: Anisotropía describe cómo varían los reflejos de la capa de capa en función de la dirección, lo que hace que las iluminaciones se estiren o alineen a lo largo de una superficie en lugar de parecer circulares. Este efecto se utiliza para representar la estructura direccional de la superficie del revestimiento, como los patrones de cepillado, rayas o flujo.

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/coat/anisotropy/coatAnisotropy01.png" alt=""/><br><em>Anisotropía = 0,1</em></td>
    <td><img src="../assets/openpbrf/renders/coat/anisotropy/coatAnisotropy05.png" alt=""/><br><em>Anisotropía = 0,5</em></td>
    <td><img src="../assets/openpbrf/renders/coat/anisotropy/coatAnisotropy1.png" alt=""/><br><em>Anisotropía = 1,0</em></td>
  </tr>
</table>

* Tangente de anisotropía: La dirección de cualquier estiramiento o rayado debido al valor de Anisotropía anterior.

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/coat/tangent/coatTangent0-orange.png" alt=""/><br></td>
    <td><img src="../assets/openpbrf/renders/coat/tangent/coatTangent03-darkRed.png" alt=""/><br></td>
    <td><img src="../assets/openpbrf/renders/coat/tangent/coatTangent06-green.png" alt=""/><br></td>
  </tr>
</table>

*Diferentes orientaciones de tangente de Anisotropía.*

* Capa normal: La capa Coat se puede deformar en pequeña medida para producir la apariencia de una geometría de escala fina. Esto podría utilizarse, por ejemplo, para reproducir el aspecto de arañazos o gotas de lluvia en un material.

+++

### Pelusa

![](../assets/openpbrf/renders/fuzz/color/fuzzColorYellow.png){width="250"}

*En este ejemplo se muestra cómo la espuma, de color amarillo, es más visible en los ángulos de los ojos.*

+++Parámetros de Fuzz

* **Peso**: Al igual que con otros parámetros de Grosor, esto controla la intensidad del efecto Zumbido, con un valor entre 0 y 1. En 0, la capa Fuzz está totalmente desactivada.

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/fuzz/weight/fuzzWeight0.png" alt=""/><br><em>Peso = 0,0</em></td>
    <td><img src="../assets/openpbrf/renders/fuzz/weight/fuzzWeight05.png" alt=""/><br><em>Peso = 0,5</em></td>
    <td><img src="../assets/openpbrf/renders/fuzz/weight/fuzzWeight1.png" alt=""/><br><em>Peso = 1,0</em></td>
  </tr>
</table>

* **Color**: Determina el color del efecto Zumbido.

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/fuzz/color/fuzzColorGreen.png" alt=""/></td>
    <td><img src="../assets/openpbrf/renders/fuzz/color/fuzzColorPurple.png" alt=""/></td>
    <td><img src="../assets/openpbrf/renders/fuzz/color/fuzzColorYellow.png" alt=""/></td>
  </tr>
</table>

* **Rugosidad**: Esencialmente determina la forma de las &quot;partículas de espoleta&quot; dentro de esta capa. Cuando este valor es cercano a 0, las partículas son altas y delgadas; son más visibles cuando se visualiza la superficie desde un ángulo superficial (rasante). En valores más altos, las partículas se acercan más a la esférica; son más fácilmente visibles desde una gama más amplia de ángulos, y la superficie parece más áspera en general como resultado.

<table>
  <tr>
    <td><img src="../assets/openpbrf/renders/fuzz/roughness/fuzzRoughness01.png" alt=""/><br><em>Rugosidad = 0,1</em></td>
    <td><img src="../assets/openpbrf/renders/fuzz/roughness/fuzzRoughness05.png" alt=""/><br><em>Rugosidad = 0,5</em></td>
    <td><img src="../assets/openpbrf/renders/fuzz/roughness/fuzzRoughness1.png" alt=""/><br><em>Rugosidad = 1,0</em></td>
  </tr>
</table>

+++

## Prácticas recomendadas para la creación de materiales

Esta sección se centra en directrices prácticas para crear materiales robustos y predecibles que se comporten bien en las condiciones de iluminación, escenas y herramientas, utilizando modelos de PBR modernos y unificados como el OpenPBR. Es decir, muchas de las siguientes recomendaciones se aplican a la creación de materiales de PBR en general; algunos, sin embargo, dependen del conjunto de características específicas de los materiales de OpenPBR.

### Empieza Con Referencias Del Mundo Real

Los materiales basados físicamente son más confiables cuando se basan en la observación del mundo real. Siempre que sea posible, las decisiones del material base sobre la referencia fotográfica, los valores medidos o la observación directa de superficies similares. Esto se aplica no solo al color, sino también a la rugosidad, la reflectividad y la variación de la superficie. Trabajar a partir de referencias ayuda a anclar los materiales dentro de rangos plausibles, lo que los hace más fáciles de reutilizar y menos sensibles a los cambios en la iluminación o el entorno. También reduce la tentación de compensar los problemas de iluminación dentro del propio material.

### Tener un modelo mental de la estructura física del material al autor

OpenPBR no es simplemente una lista de parámetros que permiten diversos efectos que el artista ajustará hasta obtener el aspecto que desea. En su núcleo, se basa en una estructura fundacional, descrita en &quot;Una visión general de las capas de un material de OpenPBR&quot;, que asume un material que consiste en una estructura de capas físicas similares. Por lo tanto, es aconsejable crear materiales teniendo en cuenta este modelo y describiendo los elementos físicos de estos materiales con los parámetros del OpenPBR. Ten en cuenta de qué está hecho el material: cómo quedaría una rebanada vertical bajo un microscopio, de dónde proceden los colores y las iluminaciones, etc. Trate tanto como sea posible para anticipar cuál de los componentes del OpenPBR será necesario para lograr esta apariencia deseada. Del mismo modo, también es posible experimentar al revés, es decir, construir un material a partir de un conjunto de capas y descubrir su aspecto final.

### Crear materiales independientemente de la iluminación

Un punto fuerte clave de los flujos de trabajo de PBR es la separación de las preocupaciones entre los materiales y la iluminación. Los materiales deben describir las propiedades de la superficie, no compensar la iluminación de la escena, la exposición o el estado de ánimo. Intenta crear materiales que permanezcan estables y creíbles bajo una amplia gama de condiciones de iluminación, incluso con poca iluminación. Esta separación facilita la gestión, depuración e iteración de las escenas, especialmente en canalizaciones más grandes en las que diferentes artistas pueden manipular los materiales y la iluminación. La validación de materiales en una serie de contextos puede resultar muy útil. Un material bien creado debería almacenarse en diferentes entornos de iluminación, escalas y ángulos de cámara. Siempre que sea posible, previsualiza los materiales en más de un contexto; por ejemplo, con iluminación de estudio neutra y en una escena más dramática. Esto ayuda a revelar si la apariencia de un material está realmente basada en sus parámetros, o si se basa en una configuración específica para verse correctamente. Los materiales que se validan bien en todos los contextos son más fáciles de reutilizar y más fiables en la producción.

### Mantener los parámetros desacoplados siempre que sea posible

Los flujos de trabajo de PBR modernos tienen como objetivo minimizar las dependencias ocultas entre los parámetros. Al ajustar un valor como la rugosidad, el metal o la transmisión, el objetivo debe ser afectar solo ese aspecto específico de la apariencia del material. En la práctica, esto significa:

* Evita crear múltiples efectos visuales a partir de una única textura, a menos que exista una justificación física clara.
* Prefiera configuraciones de parámetros simples y legibles en lugar de redes estrechamente interconectadas.
* Realice los cambios de forma incremental, evaluando su impacto de forma aislada cuando sea posible. Este enfoque hace que los materiales sean más fáciles de entender, más fáciles de depurar y más predecibles cuando se reutilizan en otros contextos.

### Uso deliberado de capas

Los materiales en capas son potentes, pero también añaden complejidad. Cada capa adicional aumenta el coste visual y computacional, y puede hacer que los materiales sean más difíciles de razonar. Al colocar capas:

* Utilice capas para representar la estructura real de la superficie (por ejemplo, dust o dirt sobre un material).
* Evite apilar capas que produzcan efectos visuales similares.
* Evalúa con regularidad si una capa contribuye de forma significativa al aspecto final. Un material más simple que capta las características esenciales de una superficie suele ser más robusto que uno de capas muy altas que es difícil de controlar.

### Ten en cuenta el rendimiento, el ruido y la estabilidad

Ciertas funciones y combinaciones de materiales son inherentemente más caras o propensas al ruido, especialmente en los representadores con trazado de trazado. Cuantas más funciones se utilicen en un material, más costoso será probablemente su procesamiento. La subsuperficie, la alta rugosidad combinada con la transmisión, los efectos de varias capas, la anisotropía o la dispersión pueden aumentar el tiempo de procesamiento y la varianza. Si bien estas funciones son valiosas, deben utilizarse con cierto cuidado. En función de la configuración del artista, pueden crear ruido excesivo, inestabilidad o tiempos de procesamiento prolongados. Es importante comprender el coste de utilizar funciones avanzadas y utilizarlas cuando ofrezcan un claro valor visual.

### Desviaciones intencionales de la plausibilidad física

Si bien los valores físicamente plausibles proporcionan una base de referencia sólida, las realidades de producción a veces requieren una desviación intencional. La estilización, la legibilidad, la dirección artística o las limitaciones técnicas pueden justificar la superación de parámetros dentro de límites realistas.

Los casos específicos en los que esto es apropiado variarán ampliamente dependiendo del proyecto, el material y la intención artística, y reconocer esos momentos es en sí mismo una cuestión de juicio más que de seguimiento de reglas. Lo que importa es que la desviación sea deliberada y decidida: que entiendas de qué principio físico te estás alejando, y por qué hacerlo sirve al trabajo.

El objetivo no es socavar los principios físicos, sino doblegarlos conscientemente al servicio de un objetivo artístico o técnico claro.

## Problemas comunes y cómo evitarlos

### Pensar en ajustes preestablecidos en lugar del comportamiento de la luz

Un obstáculo común en los flujos de trabajo basados en la física es tratar los materiales como &quot;looks&quot; predefinidos en lugar de como descripciones de cómo se comporta la luz. Esto suele parecer una gran dependencia de los ajustes preestablecidos o la copia de valores de parámetros sin comprender lo que representan.

El OpenPBR se diseña en torno a interacciones explícitas de luz: reflexión, transmisión, dispersión, absorción y emisión. Cuando un material no parece correcto, la forma más eficaz de solucionar problemas es identificar cuál de estos comportamientos es responsable y ajustarlo directamente. Esto permite tomar decisiones más claras y obtener resultados más predecibles que el uso de ajustes preestablecidos o efectos de apilamiento.

### Uso del peso del specular en lugar de la rugosidad del specular

Para controlar la reflectividad de un material, puede resultar tentador empezar por ajustar el peso del Specular, pero es más aconsejable ajustar el parámetro Rugosidad del Specular.

Todos los materiales tienen reflexión de specular, y la reflexión de specular siempre tiende al 100% en ángulos de pastoreo. Además, la mayoría de los materiales dieléctricos (no metálicos) tienen un reflejo del specular muy similar, entre el 2 y el 8% a incidencia normal. La razón principal de las diferencias en la reflectividad aparente proviene en cambio de la microgeometría del material; esto se define mediante el parámetro Rugosidad del Specular.

Sin embargo, el Peso del specular sigue siendo útil como forma abreviada para ajustar el índice de refracción localmente, para emular cambios de reflectividad debidos a microoclusiones o para ajustes artísticos en etapas tardías.

### Transmisión confusa, transparencia y dispersión subsuperficial

Los efectos de paso de luz a menudo se agrupan de forma floja bajo &#39;transparencia&#39; o &#39;translucidez&#39;, pero el OpenPBR hace distinciones claras entre ellos. La transmisión describe la luz que pasa a través de un material y sale por el lado opuesto, como se ve en el vidrio, el agua o los plásticos transparentes. La dispersión subsuperficial describe la luz que entra en un material, se dispersa internamente y sale en diferentes puntos, lo que produce sombras suaves y color interno.

A nivel físico, hay dos fenómenos en juego: la dispersión, el efecto que hace que la leche aparezca blanca, y la absorción, que hace que el café aparezca negro. Cuando hay poca o ninguna dispersión, el volumen tiende a parecer más transparente, y la transmisión es una característica clave a tener en cuenta. Cuando hay mucha dispersión, el volumen tiende a parecer más reflectante, y la subsuperficie es una característica clave. Si se llevan los parámetros a valores extremos, se podría hacer que el subsuelo pareciera transparente y la transmisión pareciera opaca, pero sería muy ineficiente.

El uso de la dispersión subsuperficial donde la transmisión es más adecuada -o viceversa- puede dar lugar a materiales demasiado complejos e ineficientes de procesar. El OpenPBR separa estas conductas para que los artistas puedan elegir la que mejor se adapte a su referencia o combinarlas intencionadamente cuando sea necesario.

### Adición De Funciones Sin Una Motivación Visual Clara

Dado que el OpenPBR expone una amplia gama de comportamientos de los materiales (como capas, pelusa, efectos de película fina, dispersión subsuperficial y emisión), puede resultar tentador habilitar varias funciones a la vez. Cuando se añade sin una razón clara basada en referencias, esto puede hacer que los materiales sean más difíciles de controlar y visualmente ruidosos.

Un enfoque más fiable consiste en comenzar con el material más simple que coincida con el comportamiento de la superficie o el volumen observado, y luego añadir complejidad solo cuando falta una señal visual específica. Cada característica adicional debe corresponder a algo visible en la referencia, como fibras en los bordes o variación de color dentro de un volumen.

### Creación de materiales para una configuración de iluminación única

Los flujos de trabajo basados en la física tienen como objetivo reducir la dependencia entre los materiales y la iluminación, pero surgen problemas cuando los materiales se ajustan para verse correctamente en una sola configuración específica. Si un material requiere intensidades o ángulos de luz particulares para parecer creíble, a menudo compensa la iluminación en lugar de describir el material en sí.

Las pruebas de materiales en condiciones de iluminación variadas pueden revelar si son robustos o dependen demasiado de la escena. Los materiales creados teniendo en cuenta esta flexibilidad tienden a integrarse de forma más fluida en diferentes entornos y proyectos.

### Uso de valores de parámetros extremos sin referencias

Si bien los parámetros de OpenPBR están basados en el significado físico, llevarlos a valores extremos sin una intención clara puede llevar a resultados inestables o confusos, especialmente cuando cambia la iluminación. Cuando un material se comporta de manera impredecible, comparar las opciones de parámetros con referencias del mundo real puede ayudar a determinar si el problema es la intención artística o el uso incorrecto de los parámetros. Las decisiones fundamentadas con referencias facilitan el diagnóstico, el perfeccionamiento y el mantenimiento coherente de los materiales en todo el proyecto.

### Malentendido de las limitaciones del modelo

No todos los materiales pueden ser representados por OpenPBR. Como cualquier modelo de material, el OpenPBR es solo eso: un modelo. A pesar de que ya es razonablemente rico en características, sigue siendo crudo en comparación con la infinitamente amplia y exuberante gama de materiales que existen o que uno puede imaginar. Hay materiales que un modelo puede representar de forma instantánea, algunos que requieren más experiencia para construirse y que extienden el modelo hasta sus límites, y otros que el modelo no puede representar. En algunos casos, un artista experto puede obtener un resultado decente con algún &quot;engaño&quot;; esto suele ocurrir cuando se realizan elecciones no físicas. Pero es importante entender qué se puede y qué no se puede hacer con el modelo, y saber cuándo se hace necesaria una solución alternativa, como un material más simple o un sombreador dedicado.

### Se espera que el Modelo de material resuelva los problemas de procesamiento

No todos los problemas visuales se originan en el propio material. El ruido, la convergencia lenta o los defectos de sombreado pueden deberse a ajustes de iluminación, muestreo o procesador en lugar de a la definición de material de OpenPBR.

Aunque el OpenPBR proporciona un modelo de material físicamente coherente, no sustituye la necesidad de una configuración adecuada de iluminación y renderizado. El aislamiento de variables (por ejemplo, el ensayo de materiales con iluminación simplificada) puede ayudar a identificar si un problema reside en el material o en otro lugar.

### Los ajustes preestablecidos como herramientas de aprendizaje, no como respuestas finales

Los ajustes preestablecidos de OpenPBR se entienden mejor como herramientas de referencia y aprendizaje. Examinar los valores preestablecidos, como el metal, la rugosidad, la anisotropía o la profundidad de transmisión, ayuda a aclarar cómo se construyen los resultados visuales específicos.

Confiar en los ajustes preestablecidos como soluciones finales puede ocultar el funcionamiento real de los materiales. Su uso como puntos de partida o ejemplos analíticos fomenta una comprensión más profunda y una creación de materiales más adaptable.

## Referencias y apéndices

### Documentación de referencia

Para conocer las definiciones autorizadas, los detalles de la implementación y las especificaciones técnicas, consulte las siguientes fuentes:

* [Academy Software Foundation - OpenPBR](https://academysoftwarefoundation.github.io/OpenPBR/)
* [Documentación del OpenPBR de Autodesk (Arnold)](https://help.autodesk.com/view/ARNOL/ENU/?guid=arnold_user_guide_ac_surface_shaders_ac_open_pbr_html)
* [Documentación de Maxon OpenPBR](https://help.maxon.net/r3d/3dsmax/en-us/Content/html/Material+OpenPBR.html#StandardMaterial-Base)

Estos recursos deben considerarse como las referencias principales de la exactitud técnica y el comportamiento específico de la aplicación.

## Apéndice i: ¿Qué es la PBR?

La representación basada en la física (PBR por sus siglas en inglés) es un enfoque de representación construido alrededor de una idea simple: en lugar de depender de una configuración de iluminación específica, los materiales deben responder a la luz de forma coherente con el comportamiento de las superficies del mundo real. Los materiales PBR se han creado para que sigan siendo creíbles en una amplia variedad de entornos, lo que los hace más predecibles, reutilizables y fáciles de administrar en los procesos de producción modernos.

Una consecuencia directa de esta base en el mundo real es que los flujos de trabajo de PBR permiten a los artistas copiar la realidad, en términos de mediciones reales, en lugar de intentar adivinarla de la mejor manera posible. En iluminación, esto puede significar trabajar con unidades físicas e intensidades del mundo real en lugar de valores arbitrarios. En los flujos de trabajo de representación que se integran con el contenido fotografiado o filmado, las cámaras y los sombreadores basados en la física ayudan a conservar las características visuales de las lentes y los sensores reales. En el caso de los materiales, el mismo principio permite utilizar técnicas como la fotogrametría, en la que las superficies escaneadas se pueden mezclar perfectamente con los materiales creados manualmente, ya que ambos se describen utilizando las mismas suposiciones físicas.

Para los artistas, la PBR proporciona un lenguaje visual compartido entre herramientas, motores y renderizadores. El objetivo de un material creado con los principios de la PBR es que parezca coherente, ya se visualice en un motor en tiempo real, en un procesador con trazado de trazado o en condiciones de iluminación radicalmente diferentes, sin necesidad de un ajuste manual constante. Esta coherencia es una razón clave por la que la PBR se ha convertido en un estándar en los juegos, los efectos visuales y la visualización.

En esencia, la PBR se basa en algunas ideas físicas fundamentales sobre la luz y las superficies. La luz se trata como energía que refleja, dispersión o es absorbida por una superficie, y los sombreadores están diseñados para conservar esa energía para que los materiales no parezcan anormalmente brillantes o reflectantes. La apariencia de la superficie se ve influenciada por factores como la rugosidad microscópica, que influye en la nitidez o suavidad de los reflejos. Los flujos de trabajo de PBR también distinguen claramente entre metales y no metales, ya que estos tipos de materiales interactúan con la luz de formas fundamentalmente diferentes. La PBR se basa en parámetros que describen propiedades físicas, como el color base, la rugosidad y el metal, que el sombreador interpreta mediante modelos derivados físicamente.

Y lo que es más importante, la PBR favorece una baja interdependencia entre las distintas partes del procesamiento. Al separar la definición del material de la iluminación, los artistas evitan tener que &quot;arreglar&quot; los materiales cada vez que cambia la luz. Esta división convierte un problema complejo en otros más pequeños y manejables: la iluminación se puede ajustar independientemente de los materiales, y los materiales se pueden crear sin conocer la configuración final de la escena. A una escala más fina, los modelos de PBR modernos —incluido el OpenPBR— pretenden mantener los parámetros lo más independientes posible, lo que permite a los artistas ajustar los valores de forma aislada sin causar efectos secundarios inesperados.

En la práctica, la PBR desplaza la función del artista de compensar las peculiaridades de la iluminación o del renderizador, y pasa a describir los materiales en términos de características del mundo real. El resultado es un flujo de trabajo que favorece la coherencia sobre el ajuste específico de la escena, con un realismo que emerge naturalmente de las entradas de material bien definidas en lugar de los trucos de iluminación hechos a mano.

Para obtener más información sobre los detalles técnicos de la PBR, consulta la [Guía de PBR de Wes McDermott](https://www.adobe.com/learn/substance-3d-designer/web/the-pbr-guide-part-1).

## Apéndice ii: ¿Qué es el OpenPBR?

OpenPBR es un modelo de sombreado de superficie abierto y basado en la física diseñado para proporcionar una forma coherente y predecible de describir el aspecto de los materiales en diferentes herramientas 3D, procesadores y canalizaciones. Define un modelo de material único y completo que puede representar una amplia gama de superficies del mundo real, al tiempo que mantiene la flexibilidad de retratar superficies más fantásticas o artísticamente idiomáticas, utilizando parámetros físicamente significativos.

En esencia, OpenPBR tiene como objetivo solucionar un problema antiguo de los flujos de trabajo 3D: incoherencia de materiales entre herramientas y procesadores. Históricamente, los artistas han trabajado con varios sombreadores &quot;estándar&quot; que se comportaban de manera similar en espíritu, pero diferían en detalles, significados de parámetros e hipótesis físicas según el software o el procesador en uso. Incluso cuando dos sombreadores compartían los mismos nombres de parámetros como &quot;rugosidad&quot; o &quot;metalidad&quot;, los resultados no siempre eran coherentes. Esto dificultaba el movimiento de activos entre herramientas, la colaboración entre equipos y estudios, o el mantenimiento de la continuidad visual en canalizaciones complejas.

Estas limitaciones se sintieron en toda la comunidad 3D, y artistas, estudios y desarrolladores comenzaron a buscar soluciones. Inicialmente se trataba de una gama de enfoques un tanto dispares y variados, y este esfuerzo continuo en toda la comunidad convergió gradualmente hacia soluciones comunes. Este trabajo, así como las múltiples discusiones y decisiones conjuntas en torno a él, se formalizaron bajo un enfoque unido de la creación material: OpenPBR, un modelo de material común y abiertamente documentado que se puede implementar consistentemente en todas las aplicaciones En lugar de estar vinculado a una sola pieza de software, el OpenPBR se basa en una base compartida sobre la que se pueden construir diferentes herramientas al tiempo que se conserva el mismo comportamiento físico subyacente. Este modelo común facilita a los artistas la transferencia de materiales entre aplicaciones, la estandarización de las prácticas de desarrollo de looks en los estudios y la estabilidad visual de los activos a medida que avanzan en la producción. Sobre todo, el OpenPBR es fundamentalmente un consenso; incluso hoy, la discusión está en curso, y se busca el consenso de una amplia gama de especialistas en el sector 3D cuando se toman decisiones.

El modelo en sí se basa en los principios de la representación basada en la física (PBR por sus siglas en inglés). Esto significa que los materiales se describen en términos de cómo la luz interactúa con las superficies en el mundo real, con un énfasis en la conservación de energía, y respuestas predecibles a la iluminación, con parámetros enraizados en la óptica del mundo real, que se organizan y exponen de una manera que apoya el desarrollo de miradas prácticas en lugar de la simulación científica. Es decir, el OpenPBR define el comportamiento del propio material: lo que significan los parámetros, cómo interactúan las distintas capas y cómo responde el material bajo la luz. Las herramientas de software individuales son libres de presentar estos controles de diferentes maneras, utilizando el estilo de interfaz de usuario que parezca más apropiado, siempre y cuando el modelo de material subyacente siga siendo coherente, aunque, en la práctica, hay una lógica detrás de la denominación, agrupación y ordenación de los parámetros, y las aplicaciones específicas tienden en gran medida a respetar esto.

## Apéndice iii: Antecedentes y motivaciones de la iniciativa OpenPBR

Para entender por qué existe el OpenPBR, es útil examinar cómo ha evolucionado el sombreado físico en los últimos diez años. A medida que la PBR se convirtió en el estándar del sector, la mayoría de las herramientas 3D más importantes introdujeron sus propios sombreadores de superficie. Estos sombreadores eran en general similares en intención: su objetivo era representar materiales del mundo real mediante modelos de reflexión que conservaran la energía y exponer los parámetros al modelo físico subyacente de una manera artísticamente significativa, como el color base, la rugosidad, el metal, etc.

Hacerlo requirió muchas iteraciones, y el panorama 3D inicialmente estaba muy fragmentado, con varios responsables de departamento explorando diferentes formas de expresar los elementos visuales y avanzando en diferentes frentes. Una solución sería reemplazada por otra, hasta que los enfoques específicos surgieran como superiores, y el trabajo en diferentes áreas comenzara a converger, lo que llevaría al surgimiento de GGX, enfoques de materiales a partir de metales y, en última instancia, OpenPBR.

Paralelamente, los oleoductos de producción se interconectaron más. Los activos cada vez más necesitaban moverse entre aplicaciones de modelado, texturizado, desarrollo de looks, iluminación, renderizado y uso en tiempo real. Los estudios comenzaron a confiar más en formatos de intercambio estandarizados como USD y MaterialX, y quedó claro que un formato que permitiera el movimiento de descripciones de materiales específicamente también sería ventajoso.

La iniciativa sobre el OpenPBR se creó en respuesta a esos problemas. Representa un esfuerzo colaborativo entre Adobe y Autodesk, apoyado por la Academy Software Foundation (ASWF), para definir un modelo de sombreado de superficie única y abierta que pueda servir como punto de referencia compartido entre herramientas. El OpenPBR consolida y formaliza los conceptos de representación basada en la física con los que los artistas ya están familiarizados; estos conceptos forman las bases de un modelo unificado con un comportamiento claramente definido.

Una motivación clave detrás del OpenPBR es la coherencia. El objetivo es garantizar que el material descrito utilizando OpenPBR se comporte de forma predecible dondequiera que se implemente, sin sacrificar el control artístico o la flexibilidad creativa. Cuando un artista ajusta la rugosidad, la metalidad o la respuesta del specular, se espera que esos cambios tengan el mismo significado visual en las implementaciones compatibles.

Otra motivación importante es la durabilidad. Al estar abiertamente especificado y gobernado como un estándar de la industria, el OpenPBR está diseñado para evolucionar con el tiempo sin estar vinculado al ciclo de vida o las prioridades de un solo producto o empresa. Esto la convierte en una base más estable para la creación de activos a largo plazo, especialmente para los estudios y artistas que desean que sus materiales sigan siendo utilizables y relevantes a medida que cambian las herramientas.