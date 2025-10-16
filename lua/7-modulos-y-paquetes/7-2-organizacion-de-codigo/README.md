# Organización de código

Divide código en módulos para mantenibilidad.

**Ejemplo de la vida real**: Módulo de utilidades.

```lua
-- utils.lua
local utils = {}

function utils.sumar(a, b)
    return a + b
end

return utils

-- main.lua
local utils = require("utils")
print(utils.sumar(2, 3))
```

**Notas importantes**: Usa return para exportar. Organiza por funcionalidad.