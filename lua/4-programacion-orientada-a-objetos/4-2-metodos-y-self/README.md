# Métodos y self

Los métodos son funciones en tables, con self refiriendo al objeto.

**Sintaxis**: function tabla:metodo(parametros)

**Ejemplo de la vida real**: Método para calcular edad en años perro.

```lua
Perro = {edad = 0}
Perro.__index = Perro

function Perro:new(edad)
    local self = setmetatable({}, Perro)
    self.edad = edad
    return self
end

function Perro:edadPerro()
    return self.edad * 7
end

local perro = Perro:new(3)
print("Edad en años perro: " .. perro:edadPerro())  -- 21
```

**Notas importantes**: : automáticamente pasa self como primer parámetro.