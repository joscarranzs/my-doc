# Event loop, microtasks y macrotasks

Event loop procesa tareas. Microtasks (promesas) antes que macrotasks (setTimeout).

**Ejemplo de la vida real**: Orden de ejecución.

```javascript
console.log("1");
setTimeout(() => console.log("2"), 0);
Promise.resolve().then(() => console.log("3"));
console.log("4");
// Output: 1, 4, 3, 2
```