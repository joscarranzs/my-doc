# Memoria y optimización

Gestión de memoria: Garbage collector limpia referencias no usadas.

Optimización: Evitar leaks, usar estructuras eficientes.

**Ejemplo de la vida real**: Closure causando leak.

```javascript
function leak() {
    let grande = new Array(1000000);
    return function() {
        console.log(grande.length);
    };
}
// grande no se libera hasta que la función interna se elimine
```