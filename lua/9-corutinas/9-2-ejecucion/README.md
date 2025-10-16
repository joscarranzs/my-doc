# Ejecución (resume, yield)

resume inicia o continúa, yield pausa.

**Ejemplo de la vida real**: Generador de números.

```lua
function contador(max)
    for i = 1, max do
        print("Generando " .. i)
        coroutine.yield(i)
    end
end

local co = coroutine.create(contador)
print(coroutine.resume(co, 3))  -- "Generando 1" luego true, 1
print(coroutine.resume(co))     -- "Generando 2" luego true, 2
```

**Notas importantes**: yield devuelve control al llamador, resume lo retoma.