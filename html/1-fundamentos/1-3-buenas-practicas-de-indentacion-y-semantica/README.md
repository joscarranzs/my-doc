# Buenas prácticas de indentación y semántica

La indentación y semántica hacen el código legible y accesible.

## Indentación

Usar espacios o tabs consistentes para anidar elementos.

**Ejemplo de la vida real**: Código bien estructurado.

```html
(`<article>`)
    (`<header>`)
        (`<h1>`)Título(`</h1>`)
    (`</header>`)
    (`<section>`)
        (`<p>`)Contenido(`</p>`)
    (`</section>`)
(`</article>`)
```

## Semántica

Usar etiquetas que describan el significado del contenido, no solo apariencia.

**Ejemplo de la vida real**: Página de artículo.

```html
(`<article>`)
    (`<header>`)
        (`<h1>`)Artículo principal(`</h1>`)
        (`<p>`)Por Autor(`</p>`)
    (`</header>`)
    (`<p>`)Contenido del artículo...(`</p>`)
    (`<footer>`)
        (`<p>`)Publicado el 2023(`</p>`)
    (`</footer>`)
(`</article>`)
```

**Notas importantes**: Semántica mejora SEO, accesibilidad y mantenibilidad. Evitar `(`<div>`)` genérico cuando hay semánticos disponibles.