# Sintaxis básica y diferencias con JavaScript

TypeScript (TS) es un superset de JavaScript que añade tipado estático opcional y otras características avanzadas. Esta sección explora la sintaxis básica y las principales diferencias con JavaScript puro.

## Diferencias clave con JavaScript

- **Tipado estático**: TS requiere declarar tipos para variables, parámetros y retornos, detectando errores en tiempo de compilación.
- **Compilación**: El código TS se compila a JS, permitiendo ejecutar en cualquier entorno JS.
- **Características modernas**: TS soporta todas las features de ES6+ y añade más como enums, interfaces, generics.
- **Herramientas**: Mejor autocompletado, refactoring y detección de errores en IDEs.

**Ejemplo de la vida real**: En una aplicación de e-commerce, usar TS evita bugs como sumar strings a números accidentalmente.

```typescript
// JavaScript
let precio = 100;
let cantidad = "5";
let total = precio * cantidad; // NaN en runtime

// TypeScript
let precio: number = 100;
let cantidad: number = 5; // Error si asignas string
let total: number = precio * cantidad; // 500, detectado en compile-time
```

## Sintaxis básica

La sintaxis es similar a JS, pero con anotaciones de tipos.

- Variables: `let/const nombre: Tipo = valor;`
- Funciones: `function nombre(param: Tipo): TipoRetorno {}`
- Clases: `class Nombre { propiedad: Tipo; }`

**Ejemplo de la vida real**: Definir una función para calcular IVA.

```typescript
function calcularIVA(precio: number, tasa: number = 0.16): number {
    return precio * tasa;
}

let precioProducto: number = 200;
let iva: number = calcularIVA(precioProducto);
console.log(`IVA: ${iva}`); // IVA: 32
```

## Archivos y compilación

Archivos TS (.ts) se compilan con `tsc` a .js. Usar `tsconfig.json` para configuración.

**Notas importantes**: TS no cambia el runtime; es solo compile-time checking. Para proyectos grandes, TS mejora mantenibilidad.