# Herencia simple con metatables

La herencia se logra asignando la metatable padre como __index de la hija.

**Ejemplo de la vida real**: Clase Empleado heredando de Persona.

```lua
Empleado = {}
Empleado.__index = Empleado
setmetatable(Empleado, Persona)  -- Hereda de Persona

function Empleado:new(nombre, edad, salario)
    local self = Persona:new(nombre, edad)  -- Llama al constructor padre
    setmetatable(self, Empleado)
    self.salario = salario
    return self
end

function Empleado:mostrarSalario()
    print("Salario: $" .. self.salario)
end

local emp = Empleado:new("Juan", 30, 50000)
emp:saludar()  -- Heredado de Persona
emp:mostrarSalario()  -- Método propio
```

**Notas importantes**: La herencia es prototipal, no clásica.