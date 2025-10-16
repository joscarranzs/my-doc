# __index, __newindex y __call

__index: Lookup de claves faltantes. __newindex: Asignación de nuevas claves. __call: Llamar table como función.

**Ejemplo de la vida real**: Proxy para logging.

```lua
local mt = {
    __index = function(t, k)
        print("Accediendo a " .. k)
        return rawget(t, k)
    end,
    __newindex = function(t, k, v)
        print("Asignando " .. k .. " = " .. v)
        rawset(t, k, v)
    end
}

local t = {}
setmetatable(t, mt)
t.nombre = "Ana"  -- "Asignando nombre = Ana"
print(t.nombre)   -- "Accediendo a nombre" luego "Ana"
```

**Notas importantes**: Usa rawget/rawset para evitar recursión.