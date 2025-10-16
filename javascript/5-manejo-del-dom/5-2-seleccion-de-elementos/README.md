# Selección de elementos (getElementById, querySelector)

Métodos para encontrar elementos en el DOM.

- getElementById: Por ID único.
- querySelector: Primer elemento que coincide con selector CSS.
- querySelectorAll: Todos los elementos que coinciden.

**Ejemplo de la vida real**: Cambiando el texto de un botón al hacer clic.

```javascript
let boton = document.getElementById("miBoton");
boton.textContent = "Clic aquí";
```