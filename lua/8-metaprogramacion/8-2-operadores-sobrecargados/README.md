# Operadores sobrecargados

Usa metamethods para sobrecargar operadores como +, -, *.

**Ejemplo de la vida real**: Vectores matemáticos.

```lua
local Vector = {}
Vector.__index = Vector

function Vector:new(x, y)
    return setmetatable({x=x, y=y}, Vector)
end

Vector.__add = function(a, b)
    return Vector:new(a.x + b.x, a.y + b.y)
end

local v1 = Vector:new(1, 2)
local v2 = Vector:new(3, 4)
local suma = v1 + v2
print(suma.x, suma.y)  -- 4, 6
```

**Notas importantes**: Solo para tables. Útil en librerías matemáticas.