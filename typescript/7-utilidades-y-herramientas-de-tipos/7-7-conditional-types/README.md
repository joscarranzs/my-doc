# Conditional types

Tipos que dependen de condiciones.

**Sintaxis**: `T extends U ? X : Y`

**Ejemplo de la vida real**: Tipo basado en condición.

```typescript
type EsArray<T> = T extends any[] ? "array" : "no array";

type A = EsArray<number[]>; // "array"
type B = EsArray<string>; // "no array"
```

**Notas importantes**: Avanzado, usado en utility types.