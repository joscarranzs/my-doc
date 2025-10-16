# Scope y closures

Variables locales limitan alcance. Closures capturan scope.

**Ejemplo de la vida real**: Función fábrica.

```lua
function crearSumador(inicial)
    return function(x)
        inicial = inicial + x
        return inicial
    end
end

local sumador = crearSumador(10)
print(sumador(5))  -- 15
print(sumador(3))  -- 18
```

**Notas importantes**: Closures mantienen estado entre llamadas.