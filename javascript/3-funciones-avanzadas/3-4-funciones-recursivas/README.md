# Funciones recursivas

Una función recursiva se llama a sí misma para resolver problemas que se pueden dividir en subproblemas similares.

**Ejemplo de la vida real**: Calculando factorial de un número.

```javascript
function factorial(n) {
    if (n === 0) return 1;
    return n * factorial(n - 1);
}

console.log(factorial(5)); // 120
```

Cuidado con el stack overflow para números grandes.