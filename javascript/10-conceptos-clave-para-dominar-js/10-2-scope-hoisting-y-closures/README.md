# Scope, hoisting y closures

Scope: Alcance de variables. Hoisting: Elevación de declaraciones. Closures: Funciones que capturan scope.

**Ejemplo de la vida real**: Variable en loop con var vs let.

```javascript
for (var i = 0; i < 3; i++) {
    setTimeout(() => console.log(i), 100); // 3, 3, 3
}
for (let j = 0; j < 3; j++) {
    setTimeout(() => console.log(j), 100); // 0, 1, 2
}
```