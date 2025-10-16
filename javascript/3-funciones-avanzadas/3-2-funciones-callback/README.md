# Funciones callback

Un callback es una función pasada como argumento a otra, ejecutada después de completar una tarea.

**Ejemplo de la vida real**: Procesando datos después de cargarlos de una API.

```javascript
function cargarDatos(callback) {
    setTimeout(() => {
        let datos = [1, 2, 3];
        callback(datos);
    }, 1000);
}

cargarDatos(datos => console.log(datos)); // [1, 2, 3] después de 1s
```

Comunes en eventos y asincronía.