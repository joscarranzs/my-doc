# Type aliases

Alias para tipos complejos.

**Sintaxis**: `type Nombre = Tipo;`

**Ejemplo de la vida real**: Tipo para coordenadas.

```typescript
type Punto = {
    x: number;
    y: number;
};

type ID = string | number;

let punto: Punto = { x: 10, y: 20 };
```

**Notas importantes**: Alias no crean nuevos tipos, solo nombres. Útil para legibilidad.