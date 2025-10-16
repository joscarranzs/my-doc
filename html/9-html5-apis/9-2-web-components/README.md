# Web Components ((`<template>`), (`<slot>`), (`<shadow-dom>`))

Componentes reutilizables nativos.

## (`<template>`)

Plantilla inerte.

**Ejemplo**:

```html
(`<template id="mi-template">`)
    (`<style>`)
        .card { border: 1px solid #ccc; padding: 10px; }
    (`</style>`)
    (`<div class="card">`)
        (`<h3>`)(`<slot name="titulo">`)Título(`</slot>`)(`</h3>`)
        (`<p>`)(`<slot name="contenido">`)Contenido(`</slot>`)(`</p>`)
    (`</div>`)
(`</template>`)
```

## Custom Elements

Componentes personalizados.

**Ejemplo**:

```javascript
class MiCard extends HTMLElement {
    connectedCallback() {
        const template = document.getElementById('mi-template');
        const clone = template.content.cloneNode(true);
        this.attachShadow({mode: 'open'}).appendChild(clone);
    }
}

customElements.define('mi-card', MiCard);
```

**Uso**:

```html
(`<mi-card>`)
    (`<span slot="titulo">`)Mi Título(`</span>`)
    (`<span slot="contenido">`)Mi contenido(`</span>`)
(`</mi-card>`)
```

**Notas importantes**: Soporte moderno. Polyfills disponibles para navegadores antiguos.