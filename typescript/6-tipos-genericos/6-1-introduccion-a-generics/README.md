# Introducción a generics

Generics permiten tipos parametrizados.

**Sintaxis**: `function nombre<T>(param: T): T`

**Ejemplo de la vida real**: Función de identidad.

```typescript
function identidad<T>(valor: T): T {
    return valor;
}

let num = identidad<number>(42);
let str = identidad("Hola");
```

**Notas importantes**: T es un placeholder. TS infiere T cuando posible.