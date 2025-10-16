# Tipos genéricos avanzados

Técnicas avanzadas como conditional types.

**Ejemplo de la vida real**: Tipo que extrae retorno de función.

```typescript
type Retorno<T> = T extends (...args: any[]) => infer R ? R : never;

function suma(a: number, b: number): number {
    return a + b;
}

type SumaRetorno = Retorno<typeof suma>; // number
```

**Notas importantes**: `infer` deduce tipos. Avanzado para metaprogramación.