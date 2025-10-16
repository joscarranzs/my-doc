# Event loop y call stack

El event loop maneja la ejecución asíncrona. Call stack ejecuta funciones sincrónicamente.

**Ejemplo de la vida real**: setTimeout no bloquea el código.

```javascript
console.log("Inicio");
setTimeout(() => console.log("Después"), 0);
console.log("Fin");
// Output: Inicio, Fin, Después
```

Entender evita bugs en asincronía.