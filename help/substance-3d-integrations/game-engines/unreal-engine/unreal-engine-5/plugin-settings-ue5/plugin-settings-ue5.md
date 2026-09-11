---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/game-engines/unreal-engine/unreal-engine-5/plugin-settings-ue5.html"
breadcrumb-title: ''
description: Configure los ajustes del plugin del Substance en Unreal Engine 5 mediante Ajustes del proyecto para personalizar el funcionamiento de los plugins.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unreal Engine > Unreal Engine 5 > Plugin Settings - UE5
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Configuración del complemento - UE5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---


# Configuración del complemento - UE5

Para acceder a la configuración, vaya a Editar > Ajustes del proyecto, desplácese hacia abajo hasta la categoría Complementos y haga clic en Substance.

![](../../../../assets/screen-shot-2022-03-31-at-5-50-29-pm.png)

## Presupuesto de hardware

El presupuesto de memoria es la cantidad máxima de memoria que se utilizará para el motor del Substance. Se puede aumentar para mejorar la velocidad de procesamiento del Substance, pero consumirá más recursos del sistema. (No siempre es un aumento útil a nivel de proyecto).

Núcleos de CPU determina cuántos núcleos puede utilizar el motor del Substance. Esto incluye tanto núcleos físicos como subprocesos híper. (Si el número asignado es mayor que los núcleos disponibles en un sistema, el valor predeterminado será utilizar todos los núcleos disponibles.

## Cocina

Si se elimina el recuento de niveles de Mip durante la cocción, se modificará la forma en que se crean las texturas para un paquete. Esta configuración puede mejorar en gran medida los tiempos de carga y reducir el tamaño del paquete, ya que los niveles de textura mip más grandes ya no tendrán que cargarse. Se cargarán los LOD de menor resolución / menor y el mayor se establecerá por defecto en UE5. A continuación, los Substance se procesan a través del motor del Substance y se actualizan en tiempo de ejecución con los LOD de alta resolución.

El Substance Engine puede ser la CPU o la GPU. El motor de GPU te permitirá crear texturas en 4K. El motor de la CPU tiene un límite de 2K.

## Optimización:

Esto limita el número de sustancias asincrónicas que pueden pasarse al motor de la sustancia en cada lote. Los números más bajos agilizarán la rapidez con la que se completa y actualiza una tarea asincrónica, en la que los números más altos procesarán y procesarán por lotes varios Substance a la vez. (Cuanto mayor sea el número, más se recortan las actualizaciones de texturas porque el tiempo entre las actualizaciones es más largo).

## Procesamiento asíncrono/sincronizado

El procesamiento de sincronización es una llamada de procesamiento de bloqueo. Esto pasará una instancia de gráfico de Substance al motor de Substance que se va a volver a calcular, pero detendrá la ejecución hasta que el motor de Substance haya terminado de procesar al Substance antes de continuar con cualquier ejecución de código adicional. El resultado también se actualizará en su pantalla tan pronto como finalice el proceso.

Async agregará su gráfico a una cola y enviará varios gráficos al motor del Substance a la vez (establecidos desde la configuración del Substance) dentro de la actualización del plugin. A diferencia del procesamiento de sincronización, tan pronto como se envían, el programa sigue ejecutándose como de costumbre en lugar de esperar a que el motor del Substance esté completo. Cuando el motor del Substance ha terminado ese lote, envía los resultados de vuelta, los aplicamos a las salidas, y arrancamos otro lote.
