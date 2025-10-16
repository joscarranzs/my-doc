# Contenteditable y atributos especiales

## Explicación

contenteditable permite edición inline. Atributos como spellcheck, autocomplete.

## Ejemplo básico

```html
<div contenteditable="true">Edita este texto</div>
<input autocomplete="username">
```

## Ejemplo de la vida real

En un editor simple.

```html
<div contenteditable="true" spellcheck="true" class="editor">
    <p>Escribe aquí...</p>
</div>
```

## Notas importantes

- spellcheck activa corrección ortográfica.
- autocomplete para autocompletado.

## Mejores prácticas

- Sanitiza contenido editado.
- Proporciona toolbar.