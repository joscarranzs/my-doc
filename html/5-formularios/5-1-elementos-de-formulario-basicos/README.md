# Elementos de formulario básicos ((`<form>`), (`<input>`), (`<label>`), (`<button>`))

Los formularios permiten interacción del usuario.

## (`<form>`)

Contenedor del formulario.

**Ejemplo de la vida real**: Formulario de login.

```html
(`<form action="/login" method="post">`)
    (`<label for="usuario">`)Usuario:(`</label>`)
    (`<input type="text" id="usuario" name="usuario" required>`)
    (`<button type="submit">`)Iniciar sesión(`</button>`)
(`</form>`)
```

## Tipos de input

- **text**: Texto simple.
- **password**: Contraseña oculta.
- **email**: Validación de email.
- **number**: Números.

**Ejemplo de la vida real**: Registro de usuario.

```html
(`<input type="email" name="email" placeholder="tu@email.com">`)
(`<input type="password" name="password" minlength="8">`)
```

## (`<label>`)

Asocia texto con input.

**Ejemplo**:

```html
(`<label for="nombre">`)Nombre completo:(`</label>`)
(`<input id="nombre" name="nombre">`)
```

**Notas importantes**: Siempre usar label para accesibilidad. El atributo for debe coincidir con id del input.