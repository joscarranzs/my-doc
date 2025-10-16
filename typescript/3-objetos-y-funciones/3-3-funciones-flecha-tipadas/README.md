# Funciones flecha tipadas

Arrow functions con tipos.

**Sintaxis**: `(param: Tipo) => TipoRetorno`

**Ejemplo de la vida real**: Callbacks en arrays.

```typescript
let numeros = [1, 2, 3];
let duplicados = numeros.map((n: number): number => n * 2);
```

**Notas importantes**: Mismo scope que funciones normales, pero no tienen 'this' propio.