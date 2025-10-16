# Paths y configuración

Configurar resolución de módulos.

**Ejemplo de la vida real**: Alias de paths.

```json
// tsconfig.json
{
    "compilerOptions": {
        "baseUrl": ".",
        "paths": {
            "@utils/*": ["src/utils/*"]
        }
    }
}

// Uso
import { helper } from "@utils/helper";
```

**Notas importantes**: Simplifica imports largos.