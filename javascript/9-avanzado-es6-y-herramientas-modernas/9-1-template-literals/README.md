# Template literals

Cadenas con interpolación y multilínea.

Sintaxis: `Hola ${variable}`

**Ejemplo de la vida real**: Generando HTML dinámico.

```javascript
let nombre = "Ana";
let html = `<div>
  <h1>Hola ${nombre}</h1>
  <p>Bienvenida</p>
</div>`;
document.body.innerHTML = html;
```