# Template y slot

## Explicación

- template: Contenido que no se renderiza inicialmente.
- slot: Puntos de inserción en web components.

## Ejemplo básico

```html
<template id="myTemplate">
    <p>Hola <slot name="name">mundo</slot>!</p>
</template>
```

## Ejemplo de la vida real

En un web component.

```html
<template id="card-template">
    <div class="card">
        <h2><slot name="title">Título</slot></h2>
        <p><slot name="content">Contenido</slot></p>
    </div>
</template>
```

## Notas importantes

- template no se muestra hasta clonarse.
- slot permite contenido personalizado.

## Mejores prácticas

- Usa para componentes reutilizables.
- Combina con Shadow DOM.