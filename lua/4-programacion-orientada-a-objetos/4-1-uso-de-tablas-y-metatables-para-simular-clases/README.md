# Uso de tablas y metatables para simular clases

En Lua, no hay clases nativas, pero se simulan con tables y metatables para herencia y métodos.

**Ejemplo de la vida real**: Creando una clase "Persona".

```lua
Persona = {}
Persona.__index = Persona

function Persona:new(nombre, edad)
    local self = setmetatable({}, Persona)
    self.nombre = nombre
    self.edad = edad
    return self
end

function Persona:saludar()
    print("Hola, soy " .. self.nombre)
end

local p = Persona:new("Ana", 25)
p:saludar()  -- "Hola, soy Ana"
```

**Notas importantes**: __index permite lookup de métodos en la metatable.