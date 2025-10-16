# Metatables y metamethods básicos

Las metatables permiten definir comportamiento personalizado para tables, como operadores sobrecargados.

Se asignan con setmetatable(table, metatable).

**Ejemplo de la vida real**: Suma de vectores.

```lua
local mt = {
    __add = function(a, b)
        return {x = a.x + b.x, y = a.y + b.y}
    end
}

local v1 = {x=1, y=2}
local v2 = {x=3, y=4}
setmetatable(v1, mt)
setmetatable(v2, mt)

local suma = v1 + v2
print(suma.x, suma.y)  -- 4, 6
```

**Notas importantes**: __add es un metamethod para el operador +.