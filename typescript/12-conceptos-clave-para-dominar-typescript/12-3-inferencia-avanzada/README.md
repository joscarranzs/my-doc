# Inferencia avanzada

TS deduce tipos complejos.

**Ejemplo de la vida real**: Retorno de funciones.

```typescript
function crearLista<T>(items: T[]) {
    return {
        items,
        length: items.length
    };
}

let lista = crearLista([1, 2, 3]); // { items: number[], length: number }
```

**Notas importantes**: Reduce anotaciones manuales.