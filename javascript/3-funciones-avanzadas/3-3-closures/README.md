# Closures

Un closure es una función que recuerda el scope donde fue creada, incluso después de que ese scope haya terminado.

**Ejemplo de la vida real**: Contador privado en una app.

```javascript
function crearContador() {
    let count = 0;
    return function() {
        count++;
        return count;
    };
}

let contador = crearContador();
console.log(contador()); // 1
console.log(contador()); // 2
```

Útil para encapsulación y datos privados.