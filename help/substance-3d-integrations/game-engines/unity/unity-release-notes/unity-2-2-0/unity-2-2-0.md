---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unity/unity-release-notes/unity-2-2-0.html"
breadcrumb-title: ''
description: Revise las notas de la versión 2.2.0 del plugin Unity para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Unity Release Notes > Unity 2.2.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unity 2.2.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 0%

---


# Unity 2.2.0

## 2.2.0 Notas de la versión

**fecha de lanzamiento: 1/10/2019**

### Complemento principal:

* Substance Engine actualizado
* Estabilidad del código mejorada
* **Compatibilidad con Unity 2018.3**
* Compatibilidad con **.NET 4.x**
* Asistencia técnica para Substance Source en 2018.3
* Se ha solucionado el problema de color del Substance Source
* El gráfico y el material correspondiente ahora tienen el mismo nombre de objeto
* Mejoras añadidas en la legibilidad de la GUI de piel de Unity Pro
* Se ha agregado compatibilidad con las asignaciones de salida de material
* Se ha corregido un error con el control de sRGB
* Se ha corregido un error por el que un usuario podía eliminar todas las instancias de un gráfico.
* Se ha corregido un error por el que, al intentar procesar Substance al cambiar parámetros en tiempo de ejecución, solo se podían procesar dos a la vez.
* Al importar un paquete que contiene archivos de Substance antiguos, el complemento ahora informará al usuario de que contiene datos de Substance antiguos y eliminará los archivos del paquete cuando Unity intente importarlos (de este modo, el usuario no tendrá que eliminar todo manualmente si se rompió)
* Se ha añadido un botón &quot;Acerca de&quot; en el menú Substance para mostrar la información de compilación relacionada con el plugin del Substance
* Se ha añadido información sobre herramientas al pasar el ratón sobre la interfaz gráfica del Substance para mostrar los nombres de parámetros del Substance expuestos
* Se han añadido botones de navegación en la interfaz gráfica de usuario del Substance para vincularlos a gráficos y materiales del Substance
* Se han añadido nuevos iconos para el gráfico/material/texturas del Substance en el navegador de contenido
* Se han actualizado las miniaturas de Substance en el navegador de contenido
* Se ha eliminado el archivo .mat de la parte delantera de los nombres de materiales de Substance.
* Se ha añadido la capacidad de cambiar el nombre de gráficos y materiales de Substance
* Al cambiar la resolución de la gráfica del Substance, la ventana emergente de aplicar/revertir ya no aparecerá forzando al usuario a confirmar el cambio en ese momento
* Se ha corregido un error por el que el proceso de reflejo solo utilizaba la resolución de Substance predeterminada, en lugar de la definida por el usuario.
* Se ha añadido una advertencia al ratón sobre la interfaz gráfica de usuario del Substance que informa al usuario si el espacio de color está establecido en Gamma.
* Funcionalidad modificada de instancias gráficas de Substance: Ahora los usuarios pueden crear instancias de gráficas en un Substance sin que se les solicite cada instancia creada en la interfaz gráfica de usuario del Substance

### Scripts:

* Hemos ocultado algunas funciones que no están pensadas para la compatibilidad con scripts
* Se ha añadido la función para duplicar instancias de gráficos de Substance mediante scripts: Duplicate()
* Función agregada para consultar información de entrada de procedimientos a través de C#, devuelve una matriz de elementos &#39;InputProperties&#39;: GetInputProperties()
* Se ha añadido una función para comprobar si existe una entrada en un gráfico y devuelve verdadero/falso: HasInput(string inputName)
* Se ha añadido una función para comprobar si una entrada visible es visible, devuelve verdadero/falso: IsInputVisible(string inputName)
* El esquema de representación se ha rediseñado. Por lo tanto, RenderSubstancesAsync() ha quedado obsoleto, se ha cambiado a graphName.RenderAsync()

## Problemas conocidos:

**Complemento del Substance principal**

* El usuario debe deshabilitar &quot;Habilitar Bitcode&quot; en el menú Configuración de compilación en Xcode para compilar para iOS
* Las vistas previas de objetos de Substance en el navegador de contenido aparecen en negro cuando el destino de compilación se establece en Android/iOS
* El botón del Alpha y el regulador de vista previa de mapa Mip no aparecen en la GUI de textura que no es del Substance después de importar el plugin del Substance
* El usuario tiene que utilizar potencias de dos para definir una resolución de gráfica de Substance mediante script
* Los materiales de Substance no son persistentes cuando se exportan o importan mediante un paquete de Unity
* Los Substance no trabajan con paquetes de recursos
* Los iconos de vista previa del Substance en el navegador de recursos cambian al icono del Substance S después de una reimportación
* Si se cambia el nombre de una gráfica de Substance que tiene un material en la escena, se eliminará dicho material de los objetos en los que se coloca
* (Solo Mac) Al actualizar el plugin en Mac, se eliminan los materiales de Substance de los prefijos |

**Secuencias de comandos**

* Las secuencias de comandos no funcionan en tiempo de ejecución si el proyecto se establece en x86 en la configuración de generación
* Problemas al utilizar backend de scripts il2cpp con determinadas plataformas de compilación

**Substance Painter Live Link**

* Al crear un proyecto después de pintar con Substance Live Link, la malla pintada volverá al material predeterminado
* Canal AO no enviado con Painter Live Link
* Las mallas con varios materiales no funcionan en Unity Live Link
* La forma en que Unity LiveLink utiliza SimpleJson se bloquea con otras instancias de SimpleJson en un proyecto
