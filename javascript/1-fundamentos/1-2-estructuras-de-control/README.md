# Estructuras de control

Las estructuras de control permiten tomar decisiones y repetir acciones en el código. Incluyen condicionales para elegir caminos y bucles para iterar sobre datos.

## Condicionales (if, else, switch)

Los condicionales ejecutan código basado en condiciones.

- **if/else**: Evalúa una condición y ejecuta un bloque si es true, otro si false.
- **switch**: Compara un valor con múltiples casos.

**Ejemplo de la vida real**: En un sistema de login, verifica si el usuario es admin para mostrar opciones especiales.

```javascript
let usuario = "admin";
if (usuario === "admin") {
    console.log("Acceso completo");
} else {
    console.log("Acceso limitado");
}

switch (usuario) {
    case "admin":
        console.log("Panel de administración");
        break;
    case "user":
        console.log("Perfil de usuario");
        break;
    default:
        console.log("Usuario desconocido");
}
```

## Bucles (for, while, do...while, for...of, for...in)

Los bucles repiten código hasta que una condición se cumpla.

- **for**: Bucle con contador.
- **while**: Bucle mientras condición sea true.
- **do...while**: Ejecuta al menos una vez, luego mientras condición.
- **for...of**: Itera sobre arrays.
- **for...in**: Itera sobre propiedades de objetos.

**Ejemplo de la vida real**: Procesando una lista de productos en un carrito de compras para calcular el total.

```javascript
let productos = [10, 20, 30];
let total = 0;

for (let precio of productos) {
    total += precio;
}
console.log(total); // 60

let i = 0;
while (i < productos.length) {
    console.log(productos[i]);
    i++;
}
```