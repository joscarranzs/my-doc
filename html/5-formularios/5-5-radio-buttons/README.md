# Radio buttons ((`<input type="radio">`))

Selección única de opciones mutuamente excluyentes.

**Ejemplo de la vida real**: Selección de género.

```html
(`<fieldset>`)
    (`<legend>`)Género:(`</legend>`)
    (`<input type="radio" id="masculino" name="genero" value="M">`)
    (`<label for="masculino">`)Masculino(`</label>`)
    (`<input type="radio" id="femenino" name="genero" value="F">`)
    (`<label for="femenino">`)Femenino(`</label>`)
    (`<input type="radio" id="otro" name="genero" value="O">`)
    (`<label for="otro">`)Otro(`</label>`)
(`</fieldset>`)
```

**Notas importantes**: Todos los radio buttons del grupo deben tener el mismo name. Solo uno puede estar checked.