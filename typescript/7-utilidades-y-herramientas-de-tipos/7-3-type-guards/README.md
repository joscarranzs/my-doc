# Type guards (typeof, instanceof, in)

Funciones que verifican tipos en runtime.

**Ejemplo de la vida real**: Procesar uniones.

```typescript
function procesar(valor: string | number) {
    if (typeof valor === "string") {
        return valor.toUpperCase();
    } else {
        return valor * 2;
    }
}

class Perro {
    ladrar() {}
}

function esPerro(obj: any): obj is Perro {
    return obj && typeof obj.ladrar === "function";
}
```

**Notas importantes**: `is` en type guards refina el tipo.