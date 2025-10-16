# Proxy y Reflect

Proxy intercepta operaciones en objetos. Reflect realiza operaciones.

**Ejemplo de la vida real**: Validando acceso a propiedades.

```javascript
let handler = {
    get: function(target, prop) {
        if (prop in target) return target[prop];
        throw new Error(`Propiedad ${prop} no existe`);
    }
};

let obj = new Proxy({}, handler);
console.log(obj.nombre); // Error
```