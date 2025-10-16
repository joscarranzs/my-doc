# Sintaxis básica

Esta sección cubre los elementos fundamentales de la sintaxis de JavaScript, incluyendo cómo declarar variables, los tipos de datos disponibles, operadores para realizar cálculos y comparaciones, y cómo agregar comentarios al código.

## Variables (let, const, var)

Las variables son contenedores que almacenan valores en la memoria. JavaScript tiene tres formas de declarar variables:

- **var**: La forma original. Tiene scope de función y puede ser redeclarada. No se recomienda en código moderno debido a posibles errores.
- **let**: Introducida en ES6. Tiene scope de bloque (como dentro de un if o loop). Puede ser reasignada pero no redeclarada en el mismo bloque.
- **const**: Para valores constantes. Debe ser inicializada al declarar y no puede ser reasignada.

**Ejemplo de la vida real**: Imagina que estás desarrollando una app de e-commerce. Usas `let` para el precio de un producto que puede cambiar con descuentos, `const` para el porcentaje de IVA que nunca cambia, y evitas `var` para prevenir bugs.

```javascript
let precioProducto = 50; // Puede cambiar si hay oferta
const iva = 0.16; // Siempre el mismo
var total = precioProducto * (1 + iva); // Total calculado

console.log(total); // 58
```

## Tipos de datos (number, string, boolean, null, undefined, symbol, object)

JavaScript es un lenguaje de tipado dinámico, lo que significa que las variables pueden cambiar de tipo. Los tipos principales son:

- **number**: Números enteros o decimales.
- **string**: Cadenas de texto, entre comillas simples o dobles.
- **boolean**: Verdadero o falso.
- **null**: Representa la ausencia intencional de valor.
- **undefined**: Valor por defecto de variables no inicializadas.
- **symbol**: Valores únicos e inmutables, introducidos en ES6.
- **object**: Colecciones de propiedades, incluyendo arrays y funciones.

**Ejemplo de la vida real**: En un formulario de registro, el nombre es un string, la edad un number, si acepta términos un boolean, y datos adicionales un object.

```javascript
let nombre = "Ana"; // string
let edad = 25; // number
let aceptaTerminos = true; // boolean
let datosExtra = null; // null inicialmente
let simbolo = Symbol("id"); // symbol
let usuario = { nombre: nombre, edad: edad }; // object
```

## Operadores (aritméticos, lógicos, relacionales)

Los operadores permiten realizar operaciones en valores.

- **Aritméticos**: +, -, *, /, % (módulo), ** (potencia).
- **Relacionales**: ==, ===, !=, !==, <, >, <=, >=.
- **Lógicos**: && (and), || (or), ! (not).

**Ejemplo de la vida real**: Calculando el descuento en una compra: si el total es mayor a 100, aplica 10% de descuento.

```javascript
let totalCompra = 120;
let descuento = totalCompra > 100 ? totalCompra * 0.1 : 0;
let final = totalCompra - descuento;
console.log(final); // 108
```

## Comentarios y buenas prácticas

Los comentarios explican el código sin ejecutarse. Usa // para línea o /* */ para bloque.

Buenas prácticas: Nombres descriptivos, indentación consistente, evitar var, usar const cuando sea posible.

**Ejemplo de la vida real**: Comenta por qué aplicas un descuento para que otros desarrolladores entiendan.

```javascript
// Calcula descuento si la compra supera 100
if (totalCompra > 100) {
    descuento = totalCompra * 0.1; // 10% de descuento
}
```