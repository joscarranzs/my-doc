# Closures

Una función que captura variables de su scope externo, incluso después de que ese scope termine.

**Ejemplo de la vida real**: Contador privado.

```lua
function crearContador()
    local count = 0
    return function()
        count = count + 1
        return count
    end
end

local contador = crearContador()
print(contador())  -- 1
print(contador())  -- 2
```

**Notas importantes**: Útiles para encapsulamiento y estado persistente.