# Destructuring y spread/rest

Técnicas modernas para trabajar con arrays y objetos de forma concisa.

## Destructuring

Extrae valores de arrays u objetos en variables.

**Ejemplo de la vida real**: Extrayendo datos de una API.

```javascript
let [nombre, edad] = ["Ana", 25];
console.log(nombre); // "Ana"

let { titulo, precio } = { titulo: "Libro", precio: 20 };
console.log(titulo); // "Libro"
```

## Spread/rest

- Spread (...): Expande elementos.
- Rest: Recoge elementos restantes.

**Ejemplo de la vida real**: Copiando y combinando arrays.

```javascript
let nums1 = [1, 2];
let nums2 = [3, 4];
let combinado = [...nums1, ...nums2]; // [1, 2, 3, 4]

function sumar(...numeros) {
    return numeros.reduce((a, b) => a + b);
}
console.log(sumar(1, 2, 3)); // 6
```