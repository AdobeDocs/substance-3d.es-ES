---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-3-0-0-plus.html"
breadcrumb-title: ''
description: Consulte las notas de la versión del plugin Unity 3.0.0 y posteriores para obtener más información sobre las nuevas funciones y mejoras.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 3.0.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 3.0.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4a060ee1aaa1731c04e70d5512e3271cd63d0381
workflow-type: tm+mt
source-wordcount: '1384'
ht-degree: 0%

---


# Unity 3.0.0+

## Unity 3.12.0

<b>Agregado/actualizado:</b>

* Compatibilidad con Substance 3D Connector en Unity, lo que habilita la funcionalidad Enviar a para enviar recursos entre Substance 3D Sampler y Unity.
* Compatibilidad para cambiar el nombre de los gráficos .sbsar y volver a publicarlos de Designer a Unity, lo que garantiza que los cambios realizados en Designer persistan cuando el gráfico actualizado se vuelva a importar al complemento Unity.
* Documentación para compartir archivos .sbsar entre proyectos de Unity.
* Página de contribución de la comunidad a la documentación del plugin Unity: https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/community-contributions.html.

<b>Corregido:</b>

* Problema por el que la miniatura de material de la carpeta de recursos del proyecto de Unity no se actualiza después de volver a publicar un archivo .sbsar, mostrando el material anterior en lugar del actual.

## Unity 3.11.0

<b>Agregado/actualizado:</b>

* Se ha mejorado el rendimiento de los proyectos con más de 1000 gráficos de Substance, lo que reduce significativamente los tiempos de respuesta de la interfaz de usuario al inspeccionar archivos sbsar en la carpeta Activos.
* Se ha añadido un botón de restablecimiento para revertir los archivos sbsar a su estado original, lo que mejora la eficiencia del flujo de trabajo.
* Documentación actualizada con una solución alternativa para el problema &quot;Entradas de imagen bloqueadas en 8 bits&quot;, disponible en: [Integraciones de Substance 3D en Unity: actualizando proyectos y problemas conocidos](../../../../game-engines/unity/upgrading-projects-known/upgrading-projects-known-issues.md).
* Documentación actualizada para solucionar el error &quot;Error de aserción en la expresión&quot; que se produce al navegar por las carpetas del panel en Unity: [Integraciones de Substance 3D en Unity: actualizando proyectos y problemas conocidos](../../../../game-engines/unity/upgrading-projects-known/upgrading-projects-known-issues.md).

<b>Corregido:</b>

* Se ha corregido un problema que provocaba que el plugin se rompiera en las plataformas Linux.
* Se han solucionado problemas de compatibilidad con el plugin Unity de la versión 2023.

## Unity 3.10.1

<b>Corregido:</b>

* Se ha corregido un problema por el que el Substance Engine no podía cargar debido a un problema con sbsario.dll en el complemento Substance 3D para Unity.

## Unity 3.10.0

<b>Agregado/actualizado:</b>

* Se ha actualizado la sección de comentarios de la API RenderInstanceAsync en el complemento.

<b>Corregido:</b>

* Se solucionó un problema de pérdida de memoria en el código C++ del complemento, lo que garantiza una recuperación de memoria completa al eliminar objetos.
* Se ha solucionado un problema en Linux por el que la importación del paquete del plugin Unity daba como resultado una excepción &#39;SubstanceException: Se ha dado un argumento no válido al error de la API, lo que ahora permite la importación correcta de archivos SBSAR.
* Se ha resuelto un problema por el que SubstanceGraphSO.CurrentStatePreset no funcionaba correctamente al cargar ajustes preestablecidos con un script de ventana del editor personalizado en Unity; ahora hay disponible un script correctivo en nuestra página Documentación para el Substance (HelpX) : https://experienceleague.adobe.com/es/docs/substance-3d/ecosystem/game-engines/unity/substance-3d-for-unity-scripting/substance-3d-for-unity-scripting
* Se ha corregido un error por el que las propiedades de los gráficos desaparecían al volver a seleccionarlas en el editor de Unity.
* Se solucionó el problema del &quot;Tipo administrado desconocido al que se hace referencia&quot; relacionado con SubstanceGraphSO en el complemento Unity, lo que mejoró la compatibilidad y la funcionalidad en las plataformas Android, en particular para Unity 2022.1 y posiblemente en todas las versiones de Unity.
* Se ha corregido un problema por el que la selección &quot;FORMATO NORMAL&quot; de la sección PARÁMETROS TÉCNICOS se mostraba incorrectamente como un campo de entrada de número, en lugar de la lista desplegable esperada con las opciones DirectX y OpenGL.

## Unity 3.9.0

<b>Agregado/actualizado:</b>

* Los archivos SBSAR ahora se pueden arrastrar y soltar en el proyecto. El objeto .sbsar se puede aplicar a una malla como se esperaba en Unity 2022.3.
* Documentación mejorada del complemento.

<b>Corregido:</b>

* Se ha corregido un problema por el que el complemento Unity no funcionaba en Android.
* Se solucionaron las restricciones de nombres en el complemento Unity. Cuando un nombre de archivo contenía un &quot;.&quot;, el complemento no cargaba el archivo correctamente.
* Se ha corregido un problema por el que, al desmarcar &quot;Generar todas las salidas&quot;, no se eliminaba automáticamente la textura adicional.
* Se ha corregido la importación incorrecta de materiales SBSAR en proyectos estándar de Unity 2021.3. Ahora, en el proyecto de plantilla estándar, los materiales SBSAR se pueden importar en la carpeta de activos y aplicarse a una malla 3D sin errores.
* Se ha corregido la importación incorrecta de materiales SBSAR en proyectos HDRP de Unity 2021/2022. Ahora, en el proyecto de plantilla HDRP, los materiales SBSAR se pueden importar en la carpeta de activos y aplicarse a una malla 3D sin errores.
* Se ha corregido un error de compilación al generar la compilación de Android para generar el APK: &quot;Error de compilación; consulte el resultado de error del compilador para obtener más información.&quot;
* Se ha corregido un problema que provocaba errores en el proceso del proyecto de generación en Windows.
* Se ha corregido un problema que hacía que el proceso del proyecto de generación fallara con errores en Android: UnityEditor.BuildPlayerWindow+BuildMethodException.
* Se solucionó la excepción UnityException que se producía al cambiar las entradas de SubstanceGraph en tiempo de ejecución. Anteriormente, al invocar SubstanceRuntimeGraph.SetTexturesResolution y SubstanceRuntimeGraph.Render(), SubstanceGraph generaba resultados incorrectos.
* Se ha corregido un error tipográfico en SubstanceEditorTools.cs.

## Unity 3.8.0

<b>Agregado/actualizado:</b>

* Se ha introducido la compatibilidad con parámetros con visibilidad condicional (función Visible si).
* Se ha actualizado el motor del Substance a la versión 9.
* Documentación actualizada para solucionar un problema por el cual NativeGraph.InRenderWork no funciona en un script de ventana de editor personalizado. Puede encontrar más información aquí: [Scripts de Substance 3D para Unity: documentación de clase](../../../../game-engines/unity/3d-for-unity-scripting/class-documentation/substanceruntime-class/substanceruntime-class.md)

<b>Corregido:</b>

* Se ha resuelto un problema que afectaba a los mapas normales en proyectos de Android.
* Se ha solucionado un error por el que, al arrastrar un objeto sbsar a la vista de escena, todos los objetos con el cursor encima tenían sus materiales reemplazados por el material del objeto sbsar.
* Se ha corregido un error que provocaba un error al inspeccionar un material marcado como Solo en tiempo de ejecución en modo de ejecución y abrir la Asignación de textura de salida.

## Unity 3.7.0

<b>Agregado/actualizado:</b>

* Compatibilidad con ajustes preestablecidos incrustados y externos
* Compatibilidad con Unity 2022.2

<b>Corregido:</b>

* Error al crear un nuevo gráfico para un archivo sbsar con el botón Copiar gráfico: &quot;Transferencia recursiva inesperada de clase con scripts&quot;
* Creación de carpetas de materiales adicionales en Mac después de volver a abrir un proyecto
* La matriz de SubstanceFileSO no se actualiza al crear o eliminar instancias de gráficos
* Se muestran opciones de entrada incorrectas al duplicar un Substance
* Campos de etiqueta vacíos en las exportaciones de archivos .sbsprs
* Errores durante la exportación o importación de ajustes preestablecidos en el editor: EndLayoutGroup: Primero se debe llamar a BeginLayoutGroup.

<b>Eliminado:</b>

* Sección Canales del complemento Unity debido a la falta de valor de usuario

## Unity 3.6.0

<b>Agregado/actualizado:</b>

* La capacidad de hacer que los valores Int 4 individuales sean editables de forma independiente.

<b>Corregido:</b>

* Problema por el que los materiales volvían a un estado anterior al reabrir un proyecto
* Error en el que se mostraba el mensaje &quot;No se han encontrado gráficos&quot; al intentar modificar el gráfico de materiales
* Problema por el que los valores de entrada del parámetro Desplazamiento de rotación en la función de Tamaño físico no cambiaban
* Problema por el que las instancias de gráficos duplicadas tenían valores de GraphID incorrectos para las entradas
* Problema por el que el generador de Substance no se inicializaba correctamente en el editor al utilizar secuencias de comandos del editor (ventana del editor personalizada) para cambiar un gráfico
* Se ha producido un problema por el cual la exportación de SubstanceGraphSO.CurrentStatePreset desde un script de ventana del editor personalizado exportaba una versión en caché del gráfico
* Problema por el que los cambios de parámetros no se guardaban cuando la ventana del inspector estaba bloqueada
* Problema por el que la entrada manual del teclado en la sección Desplazamiento de posición de las opciones de Tamaño físico no afectaba al material en el modo de edición
* Error al escribir manualmente valores de parámetros en el objeto SBSAR

## Unity 3.5.0

<b>Agregado/actualizado:</b>

* Compatibilidad con usuarios para cambiar la forma en que se asignan las texturas de salida al material de Unity
* Compatibilidad de complementos con la última versión de Unity 2022.2

<b>Corregido:</b>

* Error de referencia nulo cuando los materiales tienen una entrada Int4
* Error con las entradas Int4; el valor W se asigna a Data2 en lugar de a Data3
* Tipo en el nombre de función &quot;\_OcclusionStrength&quot;

## Unity 3.4.0

<b>Agregado/actualizado:</b>

* Controles de desplazamiento de posición para trasladar la textura por la superficie en el panel tamaño físico
* Vínculos para descargar los recursos de la comunidad de Substance 3D Assets y Substance de Adobe en la configuración del proyecto

## Unity 3.3.0

<b>Agregado/actualizado:</b>

* La función de tamaño físico para HDRP, que permite aplicar y escalar materiales en función de sus tamaños reales
* Interfaz de usuario para habilitar la GPU en la configuración del proyecto

<b>Eliminado:</b>

* ID de gráfico de la mayoría de las llamadas de API

## Unity 3.2.1

<b>Corregido:</b>

* El problema con la actualización del complemento de las versiones 3.0.0 y 3.1.0 a la última versión.

## Unity 3.2.0

<b>Agregado/actualizado:</b>

* Mejora del rendimiento en la recompilación de scripts

<b>Corregido:</b>

* Error de importación de activos en el complemento Unity al importar materiales personalizados de SBSAR
* &quot;ArgumentException: El valor no está dentro del intervalo esperado&quot; error
* &quot;ArgumentOutOfRangeException: Error &quot;El índice estaba fuera del intervalo&quot;

## Unity 3.1.0

<b>Agregado/actualizado:</b>

* Mejora de rendimiento de 1,38 veces para Mac
* El motor de GPU en Mac utiliza Metal en lugar de OpenGL

<b>Corregido:</b>

* Problema de Mac en el que se voltean los canales R y B de las texturas de salida

## Unity 3.0.0

<b>Agregado/actualizado:</b>

* Compatibilidad con Apple Silicon
* Nuevo tutorial de YouTube sobre cómo usar el complemento
* Nueva documentación de scripts

<b>Corregido:</b>

* Error en la pantalla del inspector al pulsar una y otra vez el botón de aleatorización
* Entradas de texturas nulas que interrumpen actualizaciones del Substance
* Los botones de alternancia &quot;Generar todas las salidas&quot;, &quot;Generar asignaciones de Mip&quot; y &quot;Solo tiempo de ejecución&quot; no funcionan
* Problemas con los espacios de nombres
* Error de referencia nula al entrar en el modo de reproducción con el recurso de gráfico seleccionado
* Problema con HDRP y URP para la última versión 2021.3 LTS de Unity al utilizar solo materiales de tiempo de ejecución
