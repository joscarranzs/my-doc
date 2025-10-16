# Manipulación (textContent, innerHTML, style)

Cambiar contenido y apariencia de elementos.

- textContent: Texto plano.
- innerHTML: HTML interno.
- style: Propiedades CSS.

**Ejemplo de la vida real**: Actualizando el precio de un producto.

```javascript
let precio = document.querySelector(".precio");
precio.textContent = "$25.99";
precio.style.color = "green";
```