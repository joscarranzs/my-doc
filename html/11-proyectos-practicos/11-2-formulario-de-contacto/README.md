# Formulario de contacto

Crear un formulario funcional con validación.

## HTML del formulario

```html
<form action="/enviar-contacto" method="post" id="form-contacto">
    <fieldset>
        <legend>Información personal</legend>
        <label for="nombre">Nombre:</label>
        <input type="text" id="nombre" name="nombre" required>
        
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>
        
        <label for="telefono">Teléfono:</label>
        <input type="tel" id="telefono" name="telefono">
    </fieldset>
    
    <fieldset>
        <legend>Mensaje</legend>
        <label for="asunto">Asunto:</label>
        <input type="text" id="asunto" name="asunto" required>
        
        <label for="mensaje">Mensaje:</label>
        <textarea id="mensaje" name="mensaje" rows="5" required></textarea>
    </fieldset>
    
    <button type="submit">Enviar mensaje</button>
</form>
```

## Validación con JavaScript

```javascript
document.getElementById('form-contacto').addEventListener('submit', function(e) {
    const email = document.getElementById('email').value;
    const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    
    if (!emailRegex.test(email)) {
        e.preventDefault();
        alert('Email inválido');
    }
});
```

## Mejoras

- Estilos CSS atractivos.
- Envío AJAX sin recargar página.
- Mensajes de éxito/error.

**Objetivo**: Practicar formularios, validación y UX.