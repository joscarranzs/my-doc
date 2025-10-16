# Etiquetas y atributos

## Explicación

Las etiquetas HTML definen la estructura y el contenido de una página web. Los atributos proporcionan información adicional sobre los elementos.

## Ejemplo básico

```html
<p class="intro" id="main-para">Este es un párrafo con atributos.</p>
```

## Ejemplo de la vida real

En un formulario de contacto, se usan atributos para validación.

```html
<form action="/submit" method="post">
    <input type="email" name="email" required placeholder="Tu email">
    <button type="submit">Enviar</button>
</form>
```

## Notas importantes

- Los atributos van dentro de la etiqueta de apertura.
- Algunos atributos son globales, como `class`, `id`, `style`.

## Mejores prácticas

- Usa atributos semánticos.
- Mantén los nombres de atributos descriptivos.