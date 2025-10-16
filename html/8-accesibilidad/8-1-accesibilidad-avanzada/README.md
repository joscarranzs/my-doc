# Accesibilidad avanzada (ARIA, roles, landmarks)

Atributos para mejorar accesibilidad.

## ARIA básico

- **aria-label**: Etiqueta accesible.
- **aria-describedby**: Describe elemento.

**Ejemplo**:

```html
(`<button aria-label="Cerrar modal">`)×(`</button>`)
(`<input type="text" aria-describedby="ayuda-email">`)
(`<div id="ayuda-email">`)Ingresa tu email corporativo(`</div>`)
```

## Roles

Define propósito del elemento.

**Ejemplo**:

```html
(`<div role="banner">`)Cabecera(`</div>`)
(`<nav role="navigation">`)Menú(`</nav>`)
(`<main role="main">`)Contenido principal(`</main>`)
```

## Landmarks

Puntos de referencia para navegación.

**Ejemplo de la vida real**: Página compleja.

```html
(`<header role="banner">`)
    (`<nav role="navigation" aria-label="Menú principal">`)
        (`<!-- navegación -->`)
    (`</nav>`)
(`</header>`)
(`<main role="main">`)
    (`<article role="article">`)
        (`<!-- contenido -->`)
    (`</article>`)
(`</main>`)
(`<aside role="complementary">`)
    (`<!-- sidebar -->`)
(`</aside>`)
```

**Notas importantes**: Usar HTML semántico primero, ARIA como complemento. No sobrescribir semántica nativa.