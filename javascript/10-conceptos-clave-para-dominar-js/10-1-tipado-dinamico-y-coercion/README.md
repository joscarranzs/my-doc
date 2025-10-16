# Tipado dinámico y coerción

JavaScript convierte tipos automáticamente (coerción).

**Ejemplo de la vida real**: Comparaciones que pueden sorprender.

```javascript
console.log(1 == "1"); // true (coerción)
console.log(1 === "1"); // false (estricta)
```

Entender previene bugs.