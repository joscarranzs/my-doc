# Manejo de tablas como estructuras de datos

Tables son arrays, diccionarios, objetos.

**Ejemplo de la vida real**: Base de datos simple.

```lua
local db = {}
db.usuarios = {}
db.agregarUsuario = function(nombre, edad)
    table.insert(db.usuarios, {nombre = nombre, edad = edad})
end

db:agregarUsuario("Ana", 25)
print(db.usuarios[1].nombre)  -- "Ana"
```

**Notas importantes**: Versatilidad clave de Lua.