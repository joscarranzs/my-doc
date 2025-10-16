# Etiquetas y atributos

Las etiquetas HTML definen elementos, y los atributos proporcionan información adicional sobre ellos.

## Etiquetas básicas

Etiquetas como `(p)`, `(div)`, `(span)` estructuran el contenido.

**Ejemplo de la vida real**: Página de producto.

```html
(div class="producto")
    (h2)Producto(/h2)
    (p)Descripción del producto.(/p)
(/div)
```

## Atributos comunes

- **id**: Identificador único.
- **class**: Clases para CSS/JS.
- **style**: Estilos inline.
- **data-***: Atributos personalizados.

**Ejemplo de la vida real**: Formulario de contacto.

```html
(form id="contacto" action="/enviar" method="post")
    (input type="text" name="nombre" placeholder="Tu nombre" required)
    (button type="submit")Enviar(/button)
(/form)
```

**Notas importantes**: Atributos booleanos como `required` no necesitan valor. Usar minúsculas para atributos.