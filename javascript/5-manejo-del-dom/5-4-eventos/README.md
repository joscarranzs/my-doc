# Eventos (addEventListener, eventos comunes)

Los eventos responden a acciones del usuario.

- addEventListener: Escucha eventos como 'click', 'submit'.
- Eventos comunes: click, mouseover, keydown, load.

**Ejemplo de la vida real**: Mostrando un mensaje al enviar un formulario.

```javascript
let form = document.querySelector("form");
form.addEventListener("submit", function(e) {
    e.preventDefault();
    alert("Formulario enviado");
});
```