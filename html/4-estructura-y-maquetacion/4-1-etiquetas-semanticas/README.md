# Etiquetas semánticas (`(header)`, `(nav)`, `(main)`, `(section)`, `(article)`, `(aside)`, `(footer)`)

Etiquetas que dan significado estructural al contenido.

## Principales semánticas

- **(header)**: Cabecera de página o sección.
- **(nav)**: Navegación.
- **(main)**: Contenido principal.
- **(section)**: Sección genérica.
- **(article)**: Contenido independiente.
- **(aside)**: Contenido relacionado.
- **(footer)**: Pie de página.

**Ejemplo de la vida real**: Página de blog.

```html
(header)
    (h1)Mi Blog(/h1)
    (nav)
        (a href="/")Inicio(/a)
    (/nav)
(/header)
(main)
    (article)
        (h2)Artículo 1(/h2)
        (p)Contenido...(/p)
    (/article)
(/main)
(footer)
    (p)© 2023(/p)
(/footer)
```

**Notas importantes**: Mejoran SEO y accesibilidad. Reemplazan divs genéricos.