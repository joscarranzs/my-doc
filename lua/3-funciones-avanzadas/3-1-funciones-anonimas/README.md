# Funciones anónimas

Funciones sin nombre, definidas en el lugar donde se usan, útiles para callbacks y asignaciones.

**Sintaxis**: function(parametros) cuerpo end

**Ejemplo de la vida real**: Pasando una función a table.sort.

```lua
local numeros = {3, 1, 4, 1, 5}
table.sort(numeros, function(a, b) return a > b end)  -- Orden descendente
for _, num in ipairs(numeros) do print(num) end  -- 5, 4, 3, 1, 1
```

**Notas importantes**: Comunes en librerías que esperan funciones como parámetros.