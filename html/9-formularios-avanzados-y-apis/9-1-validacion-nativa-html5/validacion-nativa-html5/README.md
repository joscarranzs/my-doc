# Validación nativa HTML5

## Explicación

Validación automática en formularios usando tipos de input.

## Ejemplo básico

```html
<input type="email" required>
<input type="url">
<input type="number" min="1" max="100">
```

## Ejemplo de la vida real

En un formulario de registro.

```html
<form>
    <input type="email" name="email" required placeholder="tu@email.com">
    <input type="password" name="password" required minlength="8">
    <input type="tel" name="phone" pattern="[0-9]{9}">
    <button type="submit">Registrarse</button>
</form>
```

## Notas importantes

- Validación en cliente, no reemplaza servidor.
- Mensajes en idioma del navegador.

## Mejores prácticas

- Combina con JavaScript para UX mejor.
- Mensajes de error personalizados.