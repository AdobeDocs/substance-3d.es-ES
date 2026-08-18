---
helpx_url: "https://helpx.adobe.com/es/substance-3d-integrations/3d-applications/modo/parameters.html"
breadcrumb-title: ''
description: Modifique los parámetros de material del Substance en MODO a través del panel Propiedades del Substance para personalizar materiales.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > MODO > Parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Parámetros
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# Parámetros

Un Substance tiene un conjunto de parámetros básicos. Estos parámetros se dividen en Substance, salidas y ajustes. Se pueden encontrar en el panel Propiedades de Substance.\
El Substance del Substance Source contendrá parámetros técnicos y canales. Las opciones de canal no tienen efecto en MODO. Las salidas se activan/desactivan mediante la sección Salidas.

![](../../../assets/parameters-4.png){width="300px"}

## Substance

Un Substance tiene un conjunto de parámetros principales, que se encuentran en la categoría Substance del panel Propiedades del Substance.

* **Recargar Substance:** Este parámetro le permite volver a cargar un Substance. Está diseñado para su uso con Substance Designer. Si está trabajando en un Substance personalizado y ha añadido un nuevo ajuste o salida, puede volver a cargar el Substance recién publicado en MODO. Se añadirán los nuevos ajustes y salidas y se conservará la configuración de los ajustes anteriores.
* **Modo de Sombreado:** Estos parámetros le permiten establecer el modo de sombreado que se usará para el Substance. Principled (default), Unreal, Unity o glTF.
* **Restablecer Substance:** Este parámetro restablecerá los ajustes a la configuración predeterminada.
* **Seleccionar gráfico:** Le permite elegir qué gráfico del archivo de Substance desea usar para crear un material.
* **Cargar ajuste preestablecido:** Puede cargar un ajuste preestablecido, que configurará los parámetros de ajuste del Substance. Los ajustes preestablecidos se pueden crear con Substance Player. El archivo de ajustes preestablecidos es del tipo .sbsprs. Una vez que haya cargado un ajuste preestablecido, debe hacer clic en el menú desplegable Ajuste preestablecido y elegir el ajuste preestablecido, ya que un archivo .sbsprs puede contener varios ajustes preestablecidos.
* **Guardar ajuste preestablecido:** Le permite guardar un ajuste preestablecido
* **Seleccionar ajuste preestablecido:** Le permite elegir un ajuste preestablecido incrustado en el archivo de Substance o entre ajustes preestablecidos guardados en MODO.
* **Convertir en disco:** Este parámetro convierte las texturas generadas por el Substance en un archivo de mapa de bits.
* **Tamaño de salida:** Este parámetro cambiará dinámicamente el tamaño de la textura para ajustarla al tamaño establecido. El Substance Engine regenerará la textura al tamaño deseado.
* **Raíz aleatoria:** Este parámetro variará la generación de procedimientos del Substance. Este parámetro es ideal para crear una versión aleatoria del mismo Substance. Permite variar rápidamente los parámetros del Substance para generar una nueva versión de las texturas

## Salidas

Las opciones de Salida permiten activar o desactivar las salidas del Substance. Un resultado es lo que genera el Substance Engine y se procesa como una textura en el árbol del sombreador.

![](../../../assets/outputs-02.png){width="300px"}

## Retoques

Los ajustes son parámetros creados en el archivo del Substance y editables en MODO. Puede seleccionar canales y, en el modo elemento, utilizar el arrastre de canales para obtener los controles juntos en un controlador emergente.

![](../../../assets/haul.png){width="300px"}
