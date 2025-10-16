# Creación (coroutine.create)

Las corutinas permiten ejecución cooperativa.

**Ejemplo de la vida real**: Simulando multitarea.

```lua
local co = coroutine.create(function()
    print("Hola")
    coroutine.yield()
    print("Mundo")
end)

coroutine.resume(co)  -- "Hola"
coroutine.resume(co)  -- "Mundo"
```

**Notas importantes**: coroutine.create devuelve un thread. No es threading real.