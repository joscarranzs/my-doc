# Lectura de usuario (io.read)

io.read lee de stdin.

**Ejemplo de la vida real**: Pidiendo nombre al usuario.

```lua
io.write("Ingresa tu nombre: ")
local nombre = io.read()
print("Hola, " .. nombre .. "!")
```

**Notas importantes**: io.read() lee línea completa. Usa "*n" para números.