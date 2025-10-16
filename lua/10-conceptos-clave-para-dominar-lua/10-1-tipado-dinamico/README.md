# Tipado dinámico

Lua no declara tipos; se infieren en runtime.

**Ejemplo de la vida real**: Flexibilidad en funciones.

```lua
function procesar(dato)
    if type(dato) == "string" then
        return string.upper(dato)
    elseif type(dato) == "number" then
        return dato * 2
    end
end

print(procesar("hola"))  -- "HOLA"
print(procesar(5))       -- 10
```

**Notas importantes**: Permite código genérico, pero requiere validación.