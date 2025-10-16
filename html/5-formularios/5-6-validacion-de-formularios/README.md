# Validación de formularios `(required, pattern, min/max)`

Validación nativa del navegador.

## Atributos de validación

- ** ``(required)`` **: Campo obligatorio.
- ** ``(pattern)`` **: Expresión regular.
- ** ``(min/max)`` **: Rangos numéricos.
- ** ``(minlength/maxlength)`` **: Longitud de texto.

**Ejemplo de la vida real**: Formulario de registro.

```html
`(input type="text" name="usuario" required minlength="3" maxlength="20")`
`(input type="password" name="password" required pattern="(?=.*\d)`(?=.*[a-z])(?=.*[A-Z]).{8,}")
`(input type="number" name="edad" min="18" max="120")`
```

## Mensajes de error

Personalizar con atributos como title.

**Ejemplo**:

```html
`(input type="email" name="email" required title="Ingresa un email válido")`
```

**Notas importantes**: Validación es del lado cliente, siempre validar en servidor. Mensajes en inglés por defecto.