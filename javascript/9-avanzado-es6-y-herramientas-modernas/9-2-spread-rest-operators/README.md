# Spread/rest operators

Spread: Expande arrays/objetos. Rest: Recoge argumentos.

**Ejemplo de la vida real**: Copiando objetos sin mutar.

```javascript
let original = { a: 1, b: 2 };
let copia = { ...original, c: 3 }; // { a: 1, b: 2, c: 3 }

function sumar(...nums) {
    return nums.reduce((a, b) => a + b);
}
console.log(sumar(1, 2, 3, 4)); // 10
```