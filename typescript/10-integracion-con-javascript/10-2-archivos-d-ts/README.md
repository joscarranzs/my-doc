# Archivos .d.ts (declaration files)

Archivos de declaración para tipos.

**Ejemplo**:

```typescript
// mi-libreria.d.ts
declare module "mi-libreria" {
    export function funcion(): string;
    export class Clase {
        metodo(): void;
    }
}
```

**Notas importantes**: Para librerías sin tipos TS.