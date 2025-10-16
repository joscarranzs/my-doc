# Tablas (`(`<table>`)`, `(`<tr>`)`, `(`<th>`)`, `(`<td>`)`, `(`<caption>`)`, `(`<thead>`)`, `(`<tbody>`)`, `(`<tfoot>`)`)

Estructuras tabulares para datos.

## Estructura básica

```html
(`<table>`)
    (`<caption>`)Datos de ventas(`</caption>`)
    (`<thead>`)
        (`<tr>`)
            (`<th>`)Producto(`</th>`)
            (`<th>`)Ventas(`</th>`)
        (`</tr>`)
    (`</thead>`)
    (`<tbody>`)
        (`<tr>`)
            (`<td>`)Libro A(`</td>`)
            (`<td>`)100(`</td>`)
        (`</tr>`)
    (`</tbody>`)
    (`<tfoot>`)
        (`<tr>`)
            (`<td>`)Total(`</td>`)
            (`<td>`)100(`</td>`)
        (`</tr>`)
    (`</tfoot>`)
(`</table>`)
```

**Ejemplo de la vida real**: Tabla de horarios.

**Notas importantes**: Usar solo para datos tabulares, no layout. Incluir caption para accesibilidad.