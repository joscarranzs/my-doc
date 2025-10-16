# require y módulos estándar

require carga módulos. Lua tiene módulos como math, string, table.

**Ejemplo de la vida real**: Usando math para cálculos.

```lua
local math = require("math")
print("Raíz cuadrada de 16: " .. math.sqrt(16))
```

**Notas importantes**: require busca en package.path. Los módulos estándar no necesitan require explícito en algunos contextos.