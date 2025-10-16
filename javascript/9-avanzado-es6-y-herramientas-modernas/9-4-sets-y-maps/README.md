# Sets y Maps

Sets: Colecciones de valores únicos. Maps: Pares clave-valor.

**Ejemplo de la vida real**: Eliminando duplicados en lista de emails.

```javascript
let emails = ["a@a.com", "b@b.com", "a@a.com"];
let unicos = new Set(emails); // Set con 2 elementos

let mapa = new Map();
mapa.set("usuario1", { nombre: "Ana" });
console.log(mapa.get("usuario1")); // { nombre: "Ana" }
```