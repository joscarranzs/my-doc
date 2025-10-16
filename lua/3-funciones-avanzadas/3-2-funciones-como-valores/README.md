# Funciones como valores

En Lua, las funciones son ciudadanos de primera clase: pueden asignarse a variables, pasarse como argumentos y devolverse.

**Ejemplo de la vida real**: Creando una fábrica de funciones.

```lua
function crearMultiplicador(factor)
    return function(x) return x * factor end
end

local duplicar = crearMultiplicador(2)
print(duplicar(5))  -- 10
```

**Notas importantes**: Permite programación funcional y patrones avanzados.