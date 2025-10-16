# Textarea y checkboxes (`(textarea)`, `(input type="checkbox")`)

Para texto largo y selecciones múltiples.

## `(textarea)`

Texto multilínea.

**Ejemplo de la vida real**: Comentarios.

```html
`(label for="comentario")`Comentario:(/label)
`(textarea id="comentario" name="comentario" rows="4" cols="50" placeholder="Escribe tu comentario...")`(/textarea)
```

## ``(Checkboxes)``

Selección múltiple o booleana.

**Ejemplo de la vida real**: Preferencias.

```html
`(input type="checkbox" id="newsletter" name="newsletter" value="si")`
`(label for="newsletter")`Suscribirme al newsletter(/label)

`(h3)`Intereses:(/h3)
`(input type="checkbox" id="deporte" name="intereses" value="deporte")`
`(label for="deporte")`Deporte(/label)
`(input type="checkbox" id="musica" name="intereses" value="musica")`
`(label for="musica")`Música(/label)
```

**Notas importantes**: Para checkboxes, usar mismo name para grupo. Value define dato enviado.