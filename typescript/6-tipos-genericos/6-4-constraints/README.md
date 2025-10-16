# Constraints (extends)

Limitar tipos genéricos.

**Sintaxis**: `T extends TipoBase`

**Ejemplo de la vida real**: Función que requiere propiedad.

```typescript
interface TieneLongitud {
    length: number;
}

function obtenerLongitud<T extends TieneLongitud>(obj: T): number {
    return obj.length;
}

console.log(obtenerLongitud("Hola")); // 4
console.log(obtenerLongitud([1, 2, 3])); // 3
```

**Notas importantes**: Extends asegura que T tenga ciertas propiedades.