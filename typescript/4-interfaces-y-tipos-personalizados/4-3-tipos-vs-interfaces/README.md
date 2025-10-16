# Tipos vs interfaces (diferencias y usos)

Ambos definen formas, pero con diferencias.

## Diferencias

- **Interfaces**: Solo objetos, extendibles, mejor para contratos públicos.
- **Tipos**: Más flexibles (uniones, tuplas), no extendibles directamente.

**Ejemplo de la vida real**: Usar interfaces para clases, tipos para utilidades.

```typescript
interface Vehiculo {
    marca: string;
}

type ID = string | number;

type VehiculoConID = Vehiculo & { id: ID };
```

**Notas importantes**: Interfaces se fusionan automáticamente si se redeclaran. Tipos no.