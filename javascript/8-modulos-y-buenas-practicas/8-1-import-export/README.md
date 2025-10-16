# Import/export

Módulos permiten dividir código en archivos.

- export: Exporta funciones/variables.
- import: Importa de otros módulos.

**Ejemplo de la vida real**: Módulo de utilidades matemáticas.

```javascript
// utils.js
export function sumar(a, b) { return a + b; }

// main.js
import { sumar } from './utils.js';
console.log(sumar(2, 3));
```

Usa ES6 modules o CommonJS.