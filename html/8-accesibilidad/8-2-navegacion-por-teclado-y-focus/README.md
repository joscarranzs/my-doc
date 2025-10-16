# Navegación por teclado y focus

Asegurar usabilidad sin mouse.

## Focus visible

CSS para indicador de foco.

**Ejemplo**:

```css
button:focus {
    outline: 2px solid blue;
    outline-offset: 2px;
}
```

## Tab order

Orden lógico de navegación.

**Ejemplo HTML**:

```html
(`<header>`)
    (`<a href="#main">`)Saltar al contenido(`</a>`)
(`</header>`)
(`<main id="main" tabindex="-1">`)
    (`<!-- contenido -->`)
(`</main>`)
```

## Skip links

Enlaces para saltar secciones.

**Ejemplo**:

```html
(`<a href="#contenido-principal" class="skip-link">`)Saltar al contenido principal(`</a>`)
```

**Notas importantes**: Probar navegación con Tab. Nunca quitar outline sin reemplazo visible.