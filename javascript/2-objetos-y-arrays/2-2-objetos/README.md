# Objetos

Los objetos son colecciones de propiedades clave-valor. Permiten modelar datos complejos como usuarios o productos.

## Propiedades y métodos

- Propiedades: Valores asociados a claves.
- Métodos: Funciones dentro del objeto.

**Ejemplo de la vida real**: Representando un usuario en una red social.

```javascript
let usuario = {
    nombre: "Juan",
    edad: 30,
    saludar: function() {
        console.log("Hola, soy " + this.nombre);
    }
};

usuario.saludar(); // "Hola, soy Juan"
```

## Acceso (dot notation, bracket notation)

- Dot: objeto.propiedad
- Bracket: objeto["propiedad"]

**Ejemplo de la vida real**: Accediendo dinámicamente a propiedades.

```javascript
let campo = "edad";
console.log(usuario.nombre); // "Juan"
console.log(usuario[campo]); // 30
```

## Métodos importantes (Object.keys, Object.values, Object.entries)

- Object.keys(): Array de claves.
- Object.values(): Array de valores.
- Object.entries(): Array de pares [clave, valor].

**Ejemplo de la vida real**: Listando propiedades de un producto.

```javascript
let producto = { nombre: "Laptop", precio: 1000, stock: 5 };
console.log(Object.keys(producto)); // ["nombre", "precio", "stock"]
console.log(Object.values(producto)); // ["Laptop", 1000, 5]
console.log(Object.entries(producto)); // [["nombre", "Laptop"], ...]
```