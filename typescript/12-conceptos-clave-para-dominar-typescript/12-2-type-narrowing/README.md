# Type narrowing

Refinar tipos en bloques de código.

**Ejemplo de la vida real**: Verificar tipos.

```typescript
function procesar(dato: unknown) {
    if (typeof dato === "string") {
        // dato es string aquí
        return dato.toUpperCase();
    }
    return dato;
}
```

**Notas importantes**: TS narrow automáticamente en conditions.