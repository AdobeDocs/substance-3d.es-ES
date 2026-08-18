---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-4/plugin-settings-ue4.html"
breadcrumb-title: ''
description: Configure los ajustes del plugin del Substance en Unreal Engine 4 hasta Ajustes del proyecto para personalizar el funcionamiento de los plugins.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 4 > Plugin Settings - UE4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'Configuración del complemento: UE4'
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 0%

---


# Configuración del complemento: UE4

Para acceder a la configuración, vaya a Editar > Ajustes del proyecto, desplácese hacia abajo hasta la categoría Complementos y haga clic en Substance.

![](../../../../assets/settings-36.png){width="400px"}

## Presupuesto de hardware

El presupuesto de memoria es la cantidad máxima de memoria que se utiliza para el motor de substance. Se puede aumentar para mejorar la velocidad del procesamiento de sustancias, pero consumirá más recursos del sistema. (No siempre es un aumento útil a nivel de proyecto).

Los núcleos de CPU son el número de núcleos que el motor Substance puede utilizar. Esto incluye tanto núcleos físicos como subprocesos híper. (Si el número asignado es mayor que los núcleos disponibles en un sistema, el valor predeterminado será utilizar todos los núcleos disponibles.

## Cocina

Si se elimina el recuento de niveles de Mip durante la cocción, se modificará la forma en que se crean las texturas para un paquete. Esta configuración puede mejorar en gran medida los tiempos de carga y reducir el tamaño del paquete, ya que los niveles de textura mip más grandes ya no tendrán que cargarse. Se cargarán los LOD de menor resolución / menor y el de mayor tamaño se establecerá por defecto en el UE4. A continuación, las sustancias se procesan a través del motor de sustancias y se actualizan en tiempo de ejecución con los LOD de alta resolución.

El Substance Engine puede ser la CPU o la GPU. El motor de GPU te permitirá crear texturas en 4K. El motor de la CPU tiene un límite de 2K.

## Generación predeterminada:

El Modo de generación de Substance (SGM) controla cómo se generan las texturas. Se trata de una configuración global para Substance. El SGM se puede cambiar según el Substance en la fábrica de Substance.

**SGM al horno**: Hornea las texturas de la sustancia. Se pierde la capacidad de cambiar parámetros en tiempo de ejecución.

**SGM al cargar sincronización**: Bloquea la aplicación mientras se cargan los Substance.

**SGM al cargar sincronización y caché**: Almacena en caché un resultado intermedio de la textura en el disco.

**SGM en sincronización de carga**: Sin bloqueo. Los Substance se generan en segundo plano.

**SGM en caché y asincrónica de carga**: Almacena en caché un resultado intermedio de la textura en el disco.

***El valor predeterminado de la plataforma es Cargar asíncrono y Caché***

## Fábrica de Substance

Para cambiar el SGM de un Substance, haga clic con el botón derecho en Fábrica de Substance > Acciones de recursos > Edición en bloque mediante la matriz de propiedades. A continuación, puede cambiar el SGM.

![](../../../../assets/sgm.png){width="800px"}

## Optimización:

Esto limita el número de sustancias asincrónicas que pueden pasarse al motor de la sustancia en cada lote. Los números más bajos aceleran la rapidez con la que se completa y actualiza una tarea asincrónica, donde los números más altos procesan y procesan varias sustancias por lotes a la vez. (Cuanto mayor sea el número, más se recortan las actualizaciones de texturas porque el tiempo entre las actualizaciones es más largo).

## Procesamiento asíncrono/sincronizado

El procesamiento de sincronización es una llamada de procesamiento de bloqueo. Esto pasará una instancia de gráfico de sustancia al motor de substance que se va a volver a calcular, pero detendrá la ejecución hasta que el motor de substance haya terminado de procesar la sustancia antes de continuar con cualquier ejecución de código adicional. El resultado también se actualizará en su pantalla tan pronto como finalice el proceso.

Async agregará tu gráfico a una cola y enviará varios gráficos al motor de substance cada vez (establecidos desde substance settings) dentro de la actualización del plugin. A diferencia del procesamiento mediante sincronización, tan pronto como se envían, el programa sigue ejecutándose como de costumbre en lugar de esperar a que termine el motor de Substance. Cuando el motor de Substance ha terminado ese lote, envía los resultados de vuelta, los aplicamos a los resultados y ponemos en marcha otro lote.
