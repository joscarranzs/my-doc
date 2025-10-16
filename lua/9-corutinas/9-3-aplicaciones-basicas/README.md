# Aplicaciones básicas

Útiles para iteradores, parsers, juegos.

**Ejemplo de la vida real**: Iterador personalizado.

```lua
function iterador(t)
    local i = 0
    return function()
        i = i + 1
        return t[i]
    end
end

local t = {"a", "b", "c"}
local nextItem = iterador(t)
print(nextItem())  -- "a"
print(nextItem())  -- "b"
```

**Notas importantes**: Simplifican código asíncrono sin callbacks complejos.