# Web Components (intro)

## Explicación

Tecnología para crear componentes reutilizables.

## Ejemplo básico

```html
<custom-element></custom-element>
<script>
    class CustomElement extends HTMLElement {
        connectedCallback() {
            this.innerHTML = '<p>Componente personalizado</p>';
        }
    }
    customElements.define('custom-element', CustomElement);
</script>
```

## Ejemplo de la vida real

En una librería de componentes.

```html
<my-button variant="primary">Click me</my-button>
```

## Notas importantes

- Encapsulación con Shadow DOM.
- Reutilizables y modulares.

## Mejores prácticas

- Usa polyfills para compatibilidad.
- Documenta API del componente.