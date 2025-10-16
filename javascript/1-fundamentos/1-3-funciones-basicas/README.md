# Funciones básicas

Las funciones son bloques de código reutilizables que realizan tareas específicas. Aprende a declararlas, pasar parámetros y entender el scope.

## Declaración y expresión

- **Declaración**: function nombre() {}. Se puede llamar antes de declarar (hoisting).
- **Expresión**: const nombre = function() {}. No se hoist.

**Ejemplo de la vida real**: Una función para calcular el IVA en facturas.

```javascript
function calcularIVA(precio) {
    return precio * 0.16;
}

const calcularIVAExp = function(precio) {
    return precio * 0.16;
};

console.log(calcularIVA(100)); // 16
```

## Parámetros y retorno

Las funciones pueden recibir parámetros y devolver valores con return.

**Ejemplo de la vida real**: Función que suma dos números para totalizar gastos.

```javascript
function sumar(a, b) {
    return a + b;
}

let gasto1 = 50;
let gasto2 = 30;
console.log(sumar(gasto1, gasto2)); // 80
```

## Scope y hoisting

- **Scope**: Alcance de variables (global, función, bloque).
- **Hoisting**: Variables var y funciones declaradas se mueven al inicio.

**Ejemplo de la vida real**: Variables locales en una función no afectan el global.

```javascript
let global = "fuera";

function ejemplo() {
    let local = "dentro";
    console.log(global); // "fuera"
    console.log(local); // "dentro"
}

ejemplo();
console.log(local); // Error: local no definida
```