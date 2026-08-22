---
title: Preguntas frecuentes
description: Encuentre respuestas a preguntas habituales sobre OpenPBR y Substance 3D.
source-git-commit: a3ceb4df30f08099799bc2caecc5446d3832fc06
workflow-type: tm+mt
source-wordcount: '1424'
ht-degree: 0%

---


# OpenPBR Preguntas frecuentes

## El modelo de OpenPBR

+++¿Qué es el OpenPBR y qué versión admite Painter?

El OpenPBR es una especificación de material abierta alojada por la Academy Software Foundation, que define un modelo de sombreado estandarizado diseñado para funcionar de forma coherente en todas las aplicaciones. [La documentación de Painter contiene más información sobre el uso de OpenPBR](https://experienceleague.adobe.com/es/docs/substance-3d-painter/using/home).

+++

+++¿Qué significa cuando una aplicación afirma &quot;OpenPBR de apoyo&quot;, y cómo puedo averiguar lo bien que una aplicación específica lo apoya?

No hay un proceso de certificación formal, por lo que la reclamación puede significar cosas diferentes. En la práctica, las implementaciones varían: algunos cubren la especificación completa, otros solo un subconjunto, dejando de lado características como la película fina, la dispersión o ciertos comportamientos subsuperficiales. Tenga en cuenta también que &quot;MaterialX apoyo&quot; y &quot;apoyo de OpenPBR&quot; no son la misma cosa; una solicitud podrá ser compatible con una sin aplicar plenamente la otra.

Para averiguar qué admite realmente una aplicación específica, utilice una combinación de enfoques: comprobar las notas de la versión (la compatibilidad se añade a menudo de forma incremental); cargar el OpenPBR Shader Playground del ASWF y compararlo con un renderizado de referencia para detectar brechas superficiales rápidamente; o, en el caso de los estudios con una importante inversión en canalizaciones, pregunte directamente al proveedor sobre las funciones admitidas y su hoja de ruta.

+++

+++¿Puede el OpenPBR garantizar resultados idénticos en diferentes aplicaciones y procesadores?

No del todo, y esto es por diseño. OpenPBR define un modelo de material compartido, pero el aspecto final también se forma mediante la iluminación, los algoritmos de representación, la gestión del color y el grado en el que cada implementación se ajusta a la especificación.

En la práctica, maximizar esa garantía significa: exportación a través de USD con integración de MaterialX; Validar la ida y vuelta anticipadamente utilizando el OpenPBR Shader Playground de la ASWF en lugar de al final de la producción; confirmar los niveles de asistencia de los proveedores para cualquier función avanzada que utilice; y acordar por adelantado qué funciones se usarán y cuáles no en los materiales compartidos. La portabilidad debe ser validada activamente, no asumida.

+++

+++¿Hay materiales que el OpenPBR no pueda representar con precisión?

Sí. OpenPBR es un modelo paramétrico. Parámetros como la rugosidad, el metal y el IOR cubren la gran mayoría de los casos de uso de producción, pero no pueden replicar la precisión de los formatos de material medido como X-Rite AxF, que capturan datos ópticos reales de una muestra física. Para el trabajo de producción en general el OpenPBR está bien adaptado; para las aplicaciones que requieran una coincidencia exacta de muestras, puede ser más adecuado un formato medido.

La pintura de coches es una ilustración útil. Es posible crear pintura de coche en OpenPBR con un par de advertencias. El OpenPBR no incluye un sombreador de pintura de coche especializado, por lo que puede ser insuficiente para determinados usos del sector de la automoción. Además, simplemente depende del tipo de pintura de coche: algunas pinturas de coches siempre tendrán propiedades que quedan fuera del ámbito de cualquier sombreador determinado. Pero con esos puntos en mente, la pintura de coches mapea naturalmente en la arquitectura en capas del OpenPBR.

+++

## Configuración y conversión

+++¿Necesito aprender OpenUSD o MaterialX para usar OpenPBR?

No. Para la mayoría de los artistas, el OpenPBR es simplemente el modelo de material incorporado en las herramientas que ya utilizan. Substance 3D Painter, Maya 2025.3 y 3ds Max 2026 utilizan OpenPBRs como su material predeterminado; trabajar con él solo significa trabajar con el sombreador estándar. USD y MaterialX solo se vuelven relevantes cuando los materiales necesitan moverse entre aplicaciones. Para los flujos de trabajo de aplicación única, la compatibilidad nativa es suficiente; para las tuberías multi-DCC, USD y MaterialX proporcionan la infraestructura de intercambio, pero en gran medida detrás de escena.

Dicho esto, la ruta de intercambio más sólida para las bibliotecas de materiales compartidos es a través de USD con la integración de MaterialX, que proporciona un contenedor estandarizado e independiente del procesador para las descripciones de materiales. Los flujos de trabajo para exportar materiales como activos independientes (sin un modelo asociado, para su uso en una biblioteca compartida) aún están en desarrollo activo y no se admiten completamente en todas partes. Antes de realizar la validación en una arquitectura de biblioteca que dependa de esto, valide su canalización específica frente a las capacidades actuales.

+++

+++¿Cómo puedo crear un nuevo proyecto de OpenPBR en Substance 3D Painter?

Un proyecto creado sin una plantilla utiliza el sombreador de OpenPBR de forma predeterminada. El sombreador de OpenPBR es ahora la primera opción de la nueva ventana de proyecto, que reemplaza a ASM. También hay disponibles plantillas dedicadas para flujos de trabajo específicos (Anisotropía, Abrigo, Zumbido, Dispersión subsuperficial), e importar un archivo USD que contenga un material de OpenPBR configurará el proyecto automáticamente. Los proyectos de muestra incluidos con Substance 3D Painter también se han actualizado para utilizar el flujo de trabajo de OpenPBR, y son un buen punto de partida para familiarizarse con su funcionamiento en la práctica.

+++

+++¿Puedo convertir a OpenPBR un proyecto existente de Adobe Standard Material (ASM)?

No hay conversión automática. Los proyectos de ASM existentes mantienen su sombreado actual cuando se abren, y las plantillas de ASM siguen estando disponibles para los nuevos proyectos.

Para migrar al OpenPBR manualmente, seleccione el sombreador de OpenPBR en la ventana de configuración del sombreador y, a continuación, añada los canales de OpenPBR relevantes mediante la configuración del conjunto de texturas > Añadir o quitar canales. Una vez hecho esto, revisa tus capas existentes para asegurarte de que su contenido se dirige a los canales previstos.

+++

+++¿Es necesario actualizar mis sombreadores personalizados para el OpenPBR?

No: los sombreadores personalizados existentes siguen funcionando, ya que las bibliotecas de sombreadores relevantes están obsoletas en lugar de eliminarse. Sin embargo, se recomienda migrar a las nuevas bibliotecas de sombreadores; son más limpios y más fáciles de trabajar. Consulte el registro de cambios de API del sombreador en el menú Ayuda para obtener más información.

+++

## Uso dentro de la aplicación

+++Con tantos parámetros disponibles en el OpenPBR, ¿dónde debo centrar mi atención?

Empieza sin complicaciones. Para la mayoría de las superficies opacas, el color base, la rugosidad del Specular y la metalidad explican la mayoría de las diferencias visibles entre los materiales. Añadir IOR si la reflectividad precisa importa; Perfeccionar color de Specular si el material tiene un matiz de ángulo de pastoreo. Activa la transmisión, subsuperficie, capa, espoleta, película fina y dispersión solo cuando tengas una razón clara y basada en referencias para hacerlo, ya que cada canal adicional añade complejidad y un posible coste de renderizado. Ocultar o contraer los grupos de parámetros no utilizados mantiene el espacio de trabajo centrado y reduce el riesgo de efectos no deseados.

+++

+++Tengo un mapa de rugosidad. ¿Debo conectarlo a Rugosidad difusa de base o Rugosidad de Specular?

Rugosidad del specular : Controla la nitidez del reflejo y es el equivalente directo de la entrada de rugosidad en otros flujos de trabajo de PBR. La rugosidad difusa de base es un parámetro independiente y especializado que afecta únicamente a la dispersión difusa; para la mayoría de los flujos de trabajo, puede permanecer en su valor predeterminado.

+++

+++¿Por qué cambiar el color base no tiene ningún efecto cuando utilizo la dispersión subsuperficial?

Existe una &#39;jerarquía de prioridad&#39; que determina cuánta influencia tiene cada parámetro en la apariencia final del material. Así es:

* El metal es lo primero: cuando el valor Metal es igual a 1, las piezas Subsuperficie y Transmisión se desactivan.
* El peso de la transmisión viene después: Si el peso de la transmisión es igual a 1, Subsurface estará ausente.
* El peso subsuperficial viene después de esto.
* El color base difuso es el último: la base difusa sólo contribuye cuando ninguno de los anteriores se ha establecido en 1.

Por lo tanto, en el ejemplo indicado, si Grosor subsuperficial se establece en 1 (su valor máximo), gobernará toda la apariencia. El cambio del valor de Color base no tiene efecto porque el Difusión base básicamente no aporta nada. Por el contrario, si Metalness se establece en su valor máximo de 1, el cambio de los valores de Peso de transmisión, Peso subsuperficial y Color base de difusión no tendrá ningún efecto en el aspecto final del material. Transmisión, Subsuperficie y Difusión son todos dieléctricos (no metálicos), por lo que ajustar Metalness a 1 es eliminar cualquier contribución no metálica.

+++

+++¿Por qué la transmisión se comporta de forma inesperada? Por ejemplo, ¿por qué mi malla aparece muy oscura cuando la activo?

La causa más común es que la Profundidad de la transmisión sea demasiado baja. Este parámetro define hasta dónde viaja la luz antes de que el color de transmisión alcance la saturación completa; en valores bajos, incluso la geometría fina aparece oscura y densa. Auméntelo para que coincida con la escala física aproximada del objeto. Si el material se ve demasiado claro, ajusta el color y la Profundidad de la transmisión juntos para encontrar el equilibrio adecuado.

La dispersión puede añadir una capa adicional de complejidad. El color de transmisión no es un simple matiz: su efecto depende del recorrido de la luz por el objeto, controlado por la Profundidad de transmisión. Por su parte, Color de dispersión controla el recorrido que puede tomar una luz independiente: rebota dentro del material en lugar de pasar directamente a través de él. Como la dispersión es direccional, el resultado también cambia dependiendo de dónde se coloque la fuente de luz. Ajustar uno sin tener en cuenta el otro es una fuente común de resultados inesperados.

+++

+++He activado la película delgada, pero no veo ningún efecto. ¿Qué me estoy perdiendo?

Compruebe primero el valor del Thickness. Contrariamente, los valores más delgados producen iridiscencia más visible: la mayoría de los efectos se producen entre 0 y 1 micrómetro. Si el efecto sigue siendo sutil, ajuste el IOR, que modifica la intensidad y el color de la interferencia. Confirme también que el peso de película fina es superior a cero.

+++
