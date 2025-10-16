# Validación y atributos (required, pattern, placeholder)

## Explicación

- required: Campo obligatorio.
- pattern: Patrón de validación con regex.
- placeholder: Texto de ejemplo.

## Ejemplo básico

```html
<input type="email" required placeholder="tu@email.com">
<input type="tel" pattern="[0-9]{9}" placeholder="123456789">
```

## Ejemplo de la vida real

En un formulario de registro.

```html
<form>
    <input type="text" name="username" required placeholder="Nombre de usuario" pattern="[a-zA-Z0-9]{3,}">
    <input type="password" name="password" required placeholder="Contraseña" minlength="8">
    <button type="submit">Registrarse</button>
</form>
```

## Notas importantes

- Validación es en cliente, siempre valida en servidor.
- pattern usa expresiones regulares.

## Mejores prácticas

- Mensajes de error claros.
- Combina con JavaScript para mejor UX.