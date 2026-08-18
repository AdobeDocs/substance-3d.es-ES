---
source-git-commit: a517442244806bc6aef0f5bfb165c5d4f67341be
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---
# Conversor de Markdown a PDF

Esta carpeta contiene una secuencia de comandos de preprocesamiento y conversión para generar versiones de PDF de páginas de documentación desde este repositorio.

## Por qué existe esto

Los archivos de origen de la documentación utilizan sintaxis de marcado específica de la plataforma de Adobe (bloques de acordeón, llamadas de alerta y extensiones de atributos de imagen) que las herramientas de marcado estándar no entienden. Este script normaliza esa sintaxis y convierte el archivo a un PDF usando [md-to-pdf](https://github.com/simonhaenisch/md-to-pdf), mientras que también comprime imágenes para mantener manejable el tamaño del archivo de salida.

## Requisitos previos

- [Node.js](https://nodejs.org/) (v18 o posterior)
- Las dependencias ya están instaladas en `node_modules/`. Si necesita volver a instalarlos, ejecute `npm ci` desde esta carpeta.

## Uso

Ejecute el script desde la **raíz del repositorio**, pasando la ruta al archivo de marcado que desea convertir:

```
node "scripts/Md to PDF converter/preprocess-for-pdf.js" <path/to/file.md>
```

**Ejemplo:**

```
node "scripts/Md to PDF converter/preprocess-for-pdf.js" help/substance-3d-general/openpbr/openpbr-overview.md
```

El PDF se escribe en el **mismo directorio que el archivo de origen**. Los archivos temporales creados durante la conversión (`*.pdf-ready.md` y `_pdf-images/`) se eliminan automáticamente si se realizan correctamente. Si se produce un error en la conversión, se dejan para ayudar en la depuración.

## ¿Qué hace el script?

| Sintaxis de origen | Salida de PDF |
|---|---|
| Bloques de acordeón `+++Title` / `+++` | Encabezado de `#####` con contenido siempre visible |
| Llamadas de alerta de `>[!NOTE]` | Cita en bloque estándar con el prefijo negrita **Nota:** |
| `![](path){width="N"}` atributos de imagen | Etiqueta `<img>` conservando el ancho especificado |
| Vínculos de imagen de marcado a `.pdf` archivos | Eliminado (referencias de autodescarga solo para web) |
| Clave de frontmatter de `hold:` | Eliminados (metadatos solo de plataforma) |
| Todas las imágenes | Redimensionado hasta un máximo de 1200 px de ancho, codificado como JPEG con una calidad del 80% |
| Todas las tablas | Bordes y fondos eliminados mediante CSS insertado |
