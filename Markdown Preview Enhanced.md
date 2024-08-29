# Configuración de Markdown Preview Enhanced

## Introducción

Este documento explica la configuración personalizada que utilizaremos para la extensión Markdown Preview Enhanced en Visual Studio Code. El objetivo es mejorar la experiencia de edición y visualización de archivos Markdown.

## Configuración JSON

Añadiremos las siguientes configuraciones a nuestro `settings.json`:

```json
{
	"markdown-preview-enhanced.automaticallyShowPreviewOfMarkdownBeingEdited": true,
	"markdown-preview-enhanced.breakOnSingleNewLine": true,
	"markdown-preview-enhanced.enableEmojiSyntax": true,
	"markdown-preview-enhanced.enableWikiLinkSyntax": true,
	"markdown-preview-enhanced.frontMatterRenderingOption": "table",
	"markdown-preview-enhanced.previewTheme": "github-light.css",
	"markdown-preview-enhanced.scrollSync": true,
	"markdown-preview-enhanced.enableExtendedTableSyntax": true,
	"markdown-preview-enhanced.mathRenderingOption": "KaTeX",
	"markdown-preview-enhanced.mermaidTheme": "default",
	"markdown-preview-enhanced.codeBlockTheme": "github.css",
	"markdown-preview-enhanced.previewMode": "Single Preview",
	"workbench.editorAssociations": {
		"*.md": "vscode.markdown.preview.editor"
	}
}
```

## Explicación de las configuraciones

1. `automaticallyShowPreviewOfMarkdownBeingEdited`: true

   - Muestra automáticamente la vista previa de Markdown al abrir un archivo .md.

2. `breakOnSingleNewLine`: true

   - Mejora la legibilidad creando saltos de línea en el HTML generado para cada nueva línea en el Markdown.

3. `enableEmojiSyntax`: true

   - Permite el uso de emojis en los documentos Markdown.

4. `enableWikiLinkSyntax`: true

   - Habilita la sintaxis de enlaces wiki, útil para crear documentación interconectada.

5. `frontMatterRenderingOption`: "table"

   - Muestra el front matter como una tabla para facilitar su lectura.

6. `previewTheme`: "github-light.css"

   - Usa el tema claro de GitHub para la vista previa, que es limpio y fácil de leer.

7. `scrollSync`: true

   - Sincroniza el desplazamiento entre el editor y la vista previa.

8. `enableExtendedTableSyntax`: true

   - Permite el uso de sintaxis de tabla extendida para crear tablas más complejas.

9. `mathRenderingOption`: "KaTeX"

   - Utiliza KaTeX para renderizar fórmulas matemáticas, que es más rápido que MathJax.

10. `mermaidTheme`: "default"

    - Usa el tema por defecto para los diagramas Mermaid.

11. `codeBlockTheme`: "github.css"

    - Usa el estilo de GitHub para los bloques de código.

12. `previewMode`: "Single Preview"

    - Muestra una única vista previa para todos los editores, ahorrando espacio en pantalla.

13. `workbench.editorAssociations`: {"\*.md": "vscode.markdown.preview.editor"}
    - Esta configuración es clave para resolver el problema de la vista doble. Asocia los archivos .md directamente con la vista previa de Markdown, evitando que se abra la vista plana junto con la vista previa.

## Cómo aplicar esta configuración

1. Abre Visual Studio Code.
2. Presiona `Ctrl+,` (o `Cmd+,` en Mac) para abrir la configuración.
3. Haz clic en el icono {} en la esquina superior derecha para abrir el archivo `settings.json`.
4. Añade o modifica las configuraciones mencionadas arriba en tu `settings.json`.
5. Guarda el archivo.

Con estas configuraciones, cuando abras un archivo .md, solo verás la vista previa de Markdown, sin la vista plana adicional.

## Notas adicionales

- Si en algún momento necesitas ver o editar el código fuente Markdown, puedes hacer clic en el botón "Open Source" en la parte superior derecha de la vista previa.
- Estas configuraciones están diseñadas para mejorar la experiencia general con archivos Markdown, pero siéntete libre de ajustarlas según tus preferencias personales.
