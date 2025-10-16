# Import/export

Módulos ES6 para organizar código.

**Ejemplo de la vida real**: Módulo de utilidades.

```typescript
// utils.ts
export function sumar(a: number, b: number): number {
    return a + b;
}

export const PI = 3.14;

// main.ts
import { sumar, PI } from "./utils";
console.log(sumar(2, 3));
```

**Notas importantes**: TS soporta ES6 modules. Compila a CommonJS o AMD según configuración.