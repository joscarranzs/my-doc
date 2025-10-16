# Funciones genéricas

Funciones que operan en tipos genéricos.

**Ejemplo de la vida real**: Función de búsqueda en array.

```typescript
function encontrar<T>(array: T[], predicado: (item: T) => boolean): T | undefined {
    for (let item of array) {
        if (predicado(item)) return item;
    }
    return undefined;
}

let usuarios = [{ id: 1, nombre: "Ana" }, { id: 2, nombre: "Juan" }];
let ana = encontrar(usuarios, u => u.nombre === "Ana");
```

**Notas importantes**: Constraints pueden limitar T, ej. `T extends object`.