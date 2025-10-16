# Etiquetas semánticas (header, nav, main, section, article, aside, footer)

## Explicación

Estas etiquetas dan significado estructural al contenido.

- header: Cabecera.
- nav: Navegación.
- main: Contenido principal.
- section: Sección.
- article: Artículo independiente.
- aside: Contenido lateral.
- footer: Pie de página.

## Ejemplo básico

```html
<header>
    <h1>Sitio</h1>
</header>
<nav>
    <ul>
        <li><a href="/">Inicio</a></li>
    </ul>
</nav>
<main>
    <section>
        <h2>Sección</h2>
        <p>Contenido</p>
    </section>
</main>
<footer>
    <p>© 2023</p>
</footer>
```

## Ejemplo de la vida real

En un blog.

```html
<article>
    <header>
        <h1>Título del post</h1>
    </header>
    <p>Contenido del artículo...</p>
</article>
<aside>
    <h3>Artículos relacionados</h3>
    <ul>...</ul>
</aside>
```

## Notas importantes

- Solo un main por página.
- Mejoran SEO y accesibilidad.

## Mejores prácticas

- Usa semántica en lugar de divs.
- Estructura lógica.