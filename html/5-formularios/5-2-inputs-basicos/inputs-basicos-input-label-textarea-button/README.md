# Inputs básicos (input, label, textarea, button)

## Explicación

- input: Campo de entrada.
- label: Etiqueta para input.
- textarea: Área de texto multilínea.
- button: Botón.

## Ejemplo básico

```html
<label for="name">Nombre:</label>
<input id="name" name="name" type="text">

<label for="message">Mensaje:</label>
<textarea id="message" name="message"></textarea>

<button type="submit">Enviar</button>
```

## Ejemplo de la vida real

En un formulario de contacto.

```html
<form>
    <label for="email">Email:</label>
    <input id="email" name="email" type="email" required>
    
    <label for="comments">Comentarios:</label>
    <textarea id="comments" name="comments" rows="4"></textarea>
    
    <button type="submit">Enviar mensaje</button>
</form>
```

## Notas importantes

- label mejora accesibilidad.
- type especifica el tipo de input.

## Mejores prácticas

- Asocia label con for.
- Usa placeholder para hints.