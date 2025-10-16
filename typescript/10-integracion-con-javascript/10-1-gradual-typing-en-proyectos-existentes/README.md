# Gradual typing en proyectos existentes

Agregar TS gradualmente a JS.

**Pasos**:

1. Instalar TS.
2. Renombrar .js a .ts.
3. Agregar tipos progresivamente.
4. Usar `any` temporalmente.

**Ejemplo de la vida real**: Migrar función JS.

```typescript
// Antes: JS
function sumar(a, b) {
    return a + b;
}

// Después: TS
function sumar(a: number, b: number): number {
    return a + b;
}
```

**Notas importantes**: Permite adopción incremental.