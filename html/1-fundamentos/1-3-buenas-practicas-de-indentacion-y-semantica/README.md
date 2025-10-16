# Buenas prácticas de indentación y semántica

## Explicación

La indentación mejora la legibilidad del código HTML. La semántica se refiere al uso de etiquetas que transmiten el significado del contenido.

## Ejemplo básico

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Título</title>
</head>
<body>
    <header>
        <h1>Título principal</h1>
    </header>
    <main>
        <section>
            <h2>Sección</h2>
            <p>Contenido</p>
        </section>
    </main>
</body>
</html>
```

## Ejemplo de la vida real

En un sitio de noticias, usa semántica para estructurar artículos.

```html
<article>
    <header>
        <h1>Título de la noticia</h1>
        <time datetime="2023-10-16">16 de octubre de 2023</time>
    </header>
    <p>Contenido de la noticia...</p>
</article>
```

## Notas importantes

- Indenta con 2 o 4 espacios.
- Usa etiquetas semánticas en lugar de divs genéricos.

## Mejores prácticas

- Prioriza la semántica sobre el estilo.
- Mantén la indentación consistente.