# html, head, body

## Explicación

- `html`: El elemento raíz de un documento HTML.
- `head`: Contiene metadatos sobre el documento, como el título, enlaces a CSS, etc.
- `body`: Contiene el contenido visible de la página.

## Ejemplo básico

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Título de la página</title>
</head>
<body>
    <p>Contenido de la página</p>
</body>
</html>
```

## Ejemplo de la vida real

En un blog, el head incluye el título del post y enlaces a estilos.

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Mi Blog - Post sobre HTML</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <article>
        <h1>Aprendiendo HTML</h1>
        <p>Este es un post sobre HTML...</p>
    </article>
</body>
</html>
```

## Notas importantes

- El atributo `lang` en `html` es importante para accesibilidad y SEO.
- Todo el contenido visible va en `body`.

## Mejores prácticas

- Usa `lang` para especificar el idioma.
- Mantén el head limpio y organizado.