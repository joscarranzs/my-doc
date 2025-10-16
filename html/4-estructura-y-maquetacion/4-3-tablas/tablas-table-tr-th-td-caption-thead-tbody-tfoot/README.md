# Tablas (table, tr, th, td, caption, thead, tbody, tfoot)

## Explicación

- table: Tabla.
- tr: Fila.
- th: Celda de encabezado.
- td: Celda de datos.
- caption: Título de tabla.
- thead: Encabezado.
- tbody: Cuerpo.
- tfoot: Pie.

## Ejemplo básico

```html
<table>
    <caption>Datos de ejemplo</caption>
    <thead>
        <tr>
            <th>Nombre</th>
            <th>Edad</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Juan</td>
            <td>25</td>
        </tr>
    </tbody>
</table>
```

## Ejemplo de la vida real

En una tabla de productos.

```html
<table>
    <thead>
        <tr>
            <th>Producto</th>
            <th>Precio</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Libro</td>
            <td>$10</td>
        </tr>
    </tbody>
</table>
```

## Notas importantes

- Usa th para encabezados.
- No uses para layout.

## Mejores prácticas

- Añade caption.
- Usa scope en th.