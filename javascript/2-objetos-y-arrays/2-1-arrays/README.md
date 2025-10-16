# Arrays

Los arrays son estructuras que almacenan múltiples valores en una sola variable. Aprende a crearlos, manipularlos y iterarlos.

## Creación y métodos básicos (push, pop, shift, unshift)

- Creación: [] o new Array().
- push(): Agrega al final.
- pop(): Remueve del final.
- shift(): Remueve del inicio.
- unshift(): Agrega al inicio.

**Ejemplo de la vida real**: Gestionando una lista de tareas pendientes.

```javascript
let tareas = ["Comprar leche"];
tareas.push("Llamar al doctor"); // ["Comprar leche", "Llamar al doctor"]
tareas.unshift("Desayunar"); // ["Desayunar", "Comprar leche", "Llamar al doctor"]
tareas.pop(); // Remueve "Llamar al doctor"
console.log(tareas); // ["Desayunar", "Comprar leche"]
```

## Iteración (for, forEach, map, filter, reduce)

Métodos para recorrer arrays.

- for: Bucle tradicional.
- forEach: Ejecuta función por elemento.
- map: Crea nuevo array transformado.
- filter: Crea array con elementos que pasan condición.
- reduce: Reduce a un valor.

**Ejemplo de la vida real**: Calculando total de precios con descuento.

```javascript
let precios = [100, 200, 50];
let conDescuento = precios.map(p => p * 0.9); // [90, 180, 45]
let baratos = precios.filter(p => p < 100); // [50]
let total = precios.reduce((sum, p) => sum + p, 0); // 350
console.log(total);
```