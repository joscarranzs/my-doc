# form y métodos (GET, POST)

## Explicación

El elemento form agrupa controles de formulario. Los métodos GET y POST envían datos.

- GET: Envía datos en la URL.
- POST: Envía datos en el cuerpo de la petición.

## Ejemplo básico

```html
<form action="/submit" method="post">
    <input name="nombre">
    <button type="submit">Enviar</button>
</form>
```

## Ejemplo de la vida real

En un formulario de login.

```html
<form action="/login" method="post">
    <label for="user">Usuario:</label>
    <input id="user" name="username">
    <label for="pass">Contraseña:</label>
    <input id="pass" name="password" type="password">
    <button type="submit">Iniciar sesión</button>
</form>
```

## Notas importantes

- action especifica dónde enviar.
- GET para búsquedas, POST para cambios.

## Mejores prácticas

- Usa POST para datos sensibles.
- Valida en servidor.