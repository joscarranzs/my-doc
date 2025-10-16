# Estructura básica de un documento

Todo documento HTML comienza con una estructura básica que define el tipo de documento y sus secciones principales. Esta estructura es esencial para que los navegadores interpreten correctamente el contenido.

## `<!DOCTYPE html>`

La declaración DOCTYPE indica que el documento es HTML5. Debe ser la primera línea del archivo.

**Ejemplo de la vida real**: En cualquier página web moderna.

```html
<!DOCTYPE html>
```

**Notas importantes**: Sin DOCTYPE, el navegador entra en modo quirks, causando inconsistencias de renderizado.

## html, head, body

- **html**: Contenedor raíz del documento.
- **head**: Contiene metadatos, título, enlaces a CSS/JS.
- **body**: Contenido visible de la página.

**Ejemplo de la vida real**: Estructura básica de una página de blog.

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Mi Blog</title>
</head>
<body>
    <h1>Bienvenido a mi blog</h1>
    <p>Contenido del blog aquí.</p>
</body>
</html>
```

**Notas importantes**: El atributo `lang` en `<html>` mejora accesibilidad y SEO.

## Comentarios

Los comentarios en HTML se escriben entre `<!-- -->` y no se renderizan.

**Ejemplo de la vida real**: Documentar secciones complejas.

```html
<!-- Este es un comentario -->
<div>
    <!-- Comentario anidado -->
    Contenido
</div>
```

**Notas importantes**: Los comentarios son visibles en el código fuente, no usar para información sensible.