# Inmutabilidad y tipos

Usar readonly y tipos para inmutabilidad.

**Ejemplo de la vida real**: Estado inmutable en React.

```typescript
interface Estado {
    readonly contador: number;
    readonly usuario: string;
}

function actualizarEstado(estado: Estado, cambios: Partial<Estado>): Estado {
    return { ...estado, ...cambios };
}
```

**Notas importantes**: Previene bugs por mutación accidental.