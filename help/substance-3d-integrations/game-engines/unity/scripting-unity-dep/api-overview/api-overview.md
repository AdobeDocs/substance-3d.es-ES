---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/game-engines/unity/scripting-in-unity-deprecated/api-overview.html"
breadcrumb-title: ''
description: Información general de referencia de la API obsoleta de Substance Unity para proyectos heredados y necesidades de secuencias de comandos.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > Game Engines > Unity > Scripting in Unity (Deprecated) > API Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Resumen de API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---


# Resumen de API

## Substance.Juego

```
Using Substance.Game
```


Substance.Game es el ensamblado que contiene las clases utilizadas para scripts. Estas clases son las siguientes:

**Substance.Game.**&#x200B;**Substance**: Referencias a la barra de referencia

**Substance.Game.SubstanceGraph**: Gráfico individual en la subbarra.*(solía ser Material de procedimiento en Unity 2017)*

## Proceso de scripts

1. Crear una instancia de SubstanceGraph
1. Defina los parámetros en la instancia del gráfico.
1. Poner en cola el Substance para procesamiento: QueueForRender() agregará el gráfico de sustancia a una cola. Esta lista se procesará en la siguiente llamada a RenderAsync o RenderSync.

### Parámetros de instancia de gráfico

```
// panel color 

mySubstance.SetInputColor("paint_color", color); 

 

// panel size 

mySubstance.SetInputVector2("square_open", panelSize); 

 

// wear level 

mySubstance.SetInputFloat("wear_level", wearLevel);
```


El valor entre comillas es el parámetro Identificador definido en Substance Designer.

En el Inspector de Unity, puede pasar el ratón sobre un parámetro para mostrar información sobre herramientas que muestra el nombre del identificador definido en Substance Designer.

![](../../../../assets/tooltip-6.png)

### Poner en cola la sustancia para el procesamiento

```
// queue the substance to render 

mySubstance.QueueForRender(); 

 

//render all substances async 

Substance.Game.Substance.RenderAsync();
```


![](../../../../assets/unityscript.gif)

>[!NOTE]
>
> Actualmente, solo se admite la arquitectura x86\_64. Debe establecer x86\_64 en Configuración de compilación

![](../../../../assets/arch.png)
