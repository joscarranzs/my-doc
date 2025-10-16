# Ambient declarations (declare)

Declarar tipos para código JS externo.

**Ejemplo de la vida real**: Librería sin tipos.

```typescript
// types.d.ts
declare module "mi-libreria" {
    export function funcion(): string;
}

// Uso
import { funcion } from "mi-libreria";
```

**Notas importantes**: Archivos .d.ts para tipos globales.