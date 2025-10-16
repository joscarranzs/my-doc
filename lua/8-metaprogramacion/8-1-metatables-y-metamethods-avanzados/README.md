# Metatables y metamethods avanzados

Metamethods como __tostring, __eq permiten personalizar comportamiento.

**Ejemplo de la vida real**: Comparando objetos.

```lua
local mt = {
    __eq = function(a, b)
        return a.valor == b.valor
    end,
    __tostring = function(self)
        return "Objeto con valor " .. self.valor
    end
}

local obj1 = {valor = 10}
local obj2 = {valor = 10}
setmetatable(obj1, mt)
setmetatable(obj2, mt)

print(obj1 == obj2)  -- true
print(obj1)  -- "Objeto con valor 10"
```

**Notas importantes**: __eq para ==, __tostring para tostring().