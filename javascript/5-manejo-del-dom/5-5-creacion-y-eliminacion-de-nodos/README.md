# Creación y eliminación de nodos

Agregar o quitar elementos del DOM.

- createElement: Crea nuevo elemento.
- appendChild: Agrega al final.
- removeChild: Elimina hijo.
- remove(): Elimina el elemento.

**Ejemplo de la vida real**: Agregando items a una lista de tareas.

```javascript
let lista = document.querySelector("ul");
let item = document.createElement("li");
item.textContent = "Nueva tarea";
lista.appendChild(item);
```