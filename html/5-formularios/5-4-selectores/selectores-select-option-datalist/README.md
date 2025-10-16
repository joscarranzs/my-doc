# Selectores (select, option, datalist)

## Explicación

- select: Lista desplegable.
- option: Opción en select.
- datalist: Lista de sugerencias para input.

## Ejemplo básico

```html
<select name="country">
    <option value="es">España</option>
    <option value="mx">México</option>
</select>

<input list="browsers" name="browser">
<datalist id="browsers">
    <option value="Chrome">
    <option value="Firefox">
</datalist>
```

## Ejemplo de la vida real

En un formulario de envío.

```html
<label for="country">País:</label>
<select id="country" name="country" required>
    <option value="">Selecciona...</option>
    <option value="es">España</option>
    <option value="us">Estados Unidos</option>
</select>
```

## Notas importantes

- option value es lo que se envía.
- datalist es para autocompletado.

## Mejores prácticas

- Agrupa options con optgroup.
- Usa required si necesario.