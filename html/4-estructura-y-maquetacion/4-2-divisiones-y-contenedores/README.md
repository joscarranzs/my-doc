# Divisiones y contenedores (`(div)`, `(span)`)

Contenedores genéricos para agrupar elementos.

## (div)

Contenedor de bloque, para secciones.

**Ejemplo de la vida real**: Layout con CSS.

```html
(div class="contenedor")
    (div class="sidebar")Menú(/div)
    (div class="contenido")Texto principal(/div)
(/div)
```

## (span)

Contenedor inline, para texto.

**Ejemplo de la vida real**: Estilizar parte de texto.

```html
(p)Precio: (span class="precio")$99(/span)(/p)
```

**Notas importantes**: Usar cuando no hay semántica específica. Preferir semánticas cuando posible.