# Select y option (`(select)`, `(option)`, `(optgroup)`)

Menús desplegables para selección.

## ``(Básico)``

```html
`(label for="pais")`País:(/label)
`(select id="pais" name="pais")`
    `(option value="es")`España(/option)
    `(option value="mx")`México(/option)
    `(option value="ar")`Argentina(/option)
(/select)
```

## Con grupos

**`(optgroup)`** agrupa opciones.

**Ejemplo de la vida real**: Selección de producto.

```html
`(select name="categoria")`
    `(optgroup label="Electrónica")`
        `(option value="laptop")`Laptop(/option)
        `(option value="telefono")`Teléfono(/option)
    (/optgroup)
    `(optgroup label="Ropa")`
        `(option value="camisa")`Camisa(/option)
        `(option value="pantalon")`Pantalón(/option)
    (/optgroup)
(/select)
```

**Atributos importantes**:
- ** ``(selected)`` **: Opción preseleccionada.
- ** ``(disabled)`` **: Opción deshabilitada.

**Notas importantes**: Usar value para envío de datos. Primera option suele ser placeholder.