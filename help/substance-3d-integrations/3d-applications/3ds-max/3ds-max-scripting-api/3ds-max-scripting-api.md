---
helpx_url: "https://helpx.adobe.com/substance-3d-integrations/3d-applications/3ds-max/3ds-max-scripting-api.html"
breadcrumb-title: ''
description: Documentación de referencia de la API de scripting de Substance 3ds Max para automatizar las operaciones de materiales.
helpx_creative_field: ""
helpx_description: Ecosystems and Plugins > 3D Applications > 3ds Max > 3ds MAX Scripting API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3ds MAX Scripting API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0197b6f5f4e3ed1f2bc0e5576bd5818d04485ed5
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 2%

---


# 3ds MAX Scripting API

A continuación se muestra la lista de comandos y propiedades del nodo Substance 2.

## Propiedades:

| Propiedad | Descripción | Tipo |
| --- | --- | --- |
| nombre | Nombre del nodo Substance2. El valor predeterminado es &quot;Substance2&quot; | Cadena |

## Comandos:

| Comando | Descripción | Retorno | Tipo de valor devuelto: | Parámetro |
| --- | --- | --- | --- | --- |
| getCurrentPackageName | Obtener el nombre de archivo base del paquete cargado (archivo sbsar cargado en el nodo de gráfico) | El nombre de archivo (sin el directorio de prefijos) del paquete cargado (archivo sbsar) | Cadena |  |
| getCurrentGraphName | Obtener el nombre del gráfico actual | identificador de la instancia de gráfico actual | Cadena |  |
| getOutputsNamesFromCurrentGraph | Obtener la lista de nombres de uso de salida para salidas habilitadas | Tabla con la lista de nombres de canal para las salidas activadas | Lista |  |
| getPresetIdentifiers | Obtener la lista de ajustes preestablecidos desde el gráfico del Substance | Tabla con la lista de identificadores de cadena para todos los ajustes preestablecidos | Lista |  |
| setPackageAndGraphNames | Cargar un archivo sbsar del disco en el nodo de gráfico | Verdadero al éxito, Falso al fracaso | Booleano | ***Parámetro de cadena***: **substancePackageFilePath** Ruta de acceso al archivo sbsar en el disco ***Parámetro de cadena***: **graphInstanceNameToSelect** Identificador de cadena del gráfico |
| setInputInt | Establecer una entrada de entero con un nuevo valor |  |  | ***Parámetro entero***: **valor** Valor entero para establecer la entrada en ***parámetro de cadena***: **inputIdentifier** El identificador único de cadena de la entrada |
| setInputFloat | Establecer una entrada flotante con un nuevo valor |  |  | ***Parámetro flotante***: **valor** Valor flotante para establecer la entrada en ***parámetro de cadena***: **inputIdentifier** El identificador único de cadena de la entrada |
| setInputString | Establecer una entrada de cadena con un nuevo valor |  |  | ***Parámetro de cadena***: **valor** Valor de cadena para establecer la entrada en ***Parámetro de cadena***: **inputIdentifier** El identificador único de cadena de la entrada |
| setInputBool | Establecer una entrada booleana con un nuevo valor |  |  | ***Parámetro booleano:* valor **Valor booleano para establecer la entrada en el parámetro***String **: **inputIdentifier** Identificador único de la cadena de entrada |
| setInputVec2 | Definición de una entrada vectorial con dos elementos |  |  | ***Parámetro Point2:*****value** Valor máximo de point2 para establecer la entrada en ***Parámetro de cadena ***: **inputIdentifier** Identificador único de la cadena de entrada |
| setInputVec3 | Definición de una entrada vectorial con tres elementos |  |  | ***Parámetro Point3:* valor **Valor máximo point3 para establecer la entrada en***Parámetro String ***: **inputIdentifier** Identificador único de la cadena de entrada |
| setInputVec4 | Definición de una entrada vectorial con cuatro elementos |  |  | ***Parámetro Point4***: **valor** Valor máximo de punto4 para establecer la entrada en ***parámetro de cadena:* inputIdentifier **Identificador de cadena único de la entrada |
| setInputColor | Definir una entrada de color con un nuevo valor |  |  | ***Parámetro de color***: **valor** Valor de color máximo para establecer la entrada en ***parámetro de cadena:* inputIdentifier **Identificador de cadena único de la entrada |
| setInputComboSelection | Establecer el valor seleccionado actualmente en una entrada de cuadro combinado |  |  | ***Parámetro entero***: **valor** Índice del widget de cuadro combinado ***Parámetro de cadena***: **inputIdentifier** El identificador único de cadena de la entrada |
| getInputInt | Obtener el valor de entrada de un tipo de entrada entero | El valor entero actual de la entrada | Entero | ***Parámetro de cadena:* inputIdentifier **Identificador de cadena único de la entrada |
| getInputFloat | Obtener el valor de entrada de un tipo de entrada flotante | El valor flotante actual de la entrada | Flotante | ***Parámetro de cadena:* inputIdentifier **Identificador de cadena único de la entrada |
| getInputString | Obtener el valor de entrada de un tipo de entrada de cadena | El valor de cadena actual de la entrada | Cadena | ***Parámetro de cadena:* inputIdentifier **Identificador de cadena único de la entrada |
| getInputBool | Obtener el valor de entrada para un tipo de entrada booleano | El valor booleano actual de la entrada | Booleano | ***Parámetro de cadena:* inputIdentifier **Identificador de cadena único de la entrada |
| getInputVec2 | Obtener el valor de entrada para un tipo de entrada point2 | El valor máx. punto2 actual de la entrada | Punto2 | ***Parámetro de cadena:* inputIdentifier **Identificador de cadena único de la entrada |
| getInputVec3 | Obtener el valor de entrada de un tipo de entrada point3 | El valor actual de punto máximo3 de la entrada | Punto3 | ***Parámetro de cadena:* inputIdentifier **Identificador de cadena único de la entrada |
| getInputVec4 | Obtener el valor de entrada de un tipo de entrada point4 | El valor máximo actual de point4 de la entrada | Punto4 | ***Parámetro de cadena:* inputIdentifier **Identificador de cadena único de la entrada |
| getInputColor | Obtener el valor de entrada de un tipo de entrada de color | El valor actual de la entrada como color | Color | ***Parámetro de cadena:* inputIdentifier **Identificador de cadena único de la entrada |
| getInputComboSelection | Obtener el índice de la selección del cuadro combinado en función del identificador | Índice del elemento del cuadro combinado seleccionado | Entero | ***Parámetro de cadena:* inputIdentifier **Identificador de cadena único de la entrada |
| getMaterialDependentCount | Obtener el número de dependencias de materiales | El número de referencias dependientes que son de un tipo de material | Entero |  |
| AplicarValoresASelectedPreset | Anula el ajuste preestablecido seleccionado con los valores de entrada actuales |  |  |  |
| QuitarTodosLosAjustesPreestablecidos | Eliminar todos los ajustes preestablecidos en el nodo de gráfico actual |  |  |  |
| CreatePreset | Crear un nuevo ajuste preestablecido a partir de las entradas actuales |  |  | ***Parámetro de cadena:* newPresetName **Nombre para mostrar del nuevo ajuste preestablecido |
| RemoveOnePreset | Quitar el ajuste preestablecido con el nombre proporcionado |  |  | ***Parámetro de cadena:* selectedPresetName **Nombre del ajuste preestablecido que se va a quitar |
| ImportarAjustePreestablecido | Importar el archivo sbsprs a los ajustes preestablecidos actuales |  |  | ***Parámetro de cadena:*****filePath** Cadena que contiene la ruta del archivo desde el que se va a importar el ajuste preestablecido |
| ExportPreset**\*obsoleto** Para eliminar en la versión 2.5.0\* | Exportar el ajuste preestablecido seleccionado actualmente a un archivo sbsprs |  |  | ***Parámetro de cadena***: **filePath** Cadena que contiene la ruta de archivo a la que se va a exportar el ajuste preestablecido |
| exportPresetList | Exportar los ajustes preestablecidos dados a un único archivo de ajustes preestablecidos |  |  | ***Parámetro de cadena***: **filePath** Cadena que contiene la ruta del archivo para exportar los ajustes preestablecidos al parámetro ***List**: **ajustes preestablecidos** Lista que contiene los nombres de los ajustes preestablecidos que se van a exportar |
| HornearSalidasDeGráficoSeleccionado | Convertir los mapas de bits de la instancia de gráfico seleccionada en disco |  |  | ***Parámetro de cadena:* filePath **El directorio de la ruta raíz en el que se escriben las imágenes***Parámetro de cadena ***: **imageFormatExtension** Extensión o formato de archivo para escribir las imágenes como |
