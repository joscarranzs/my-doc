# Concatenación y longitud

Las strings en Lua son inmutables. Usa .. para concatenar y # para longitud.

**Ejemplo de la vida real**: Construyendo un mensaje de bienvenida.

```lua
local nombre = "Ana"
local mensaje = "Bienvenido, " .. nombre .. "!"
print(mensaje)  -- "Bienvenido, Ana!"
print("Longitud: " .. #mensaje)  -- Longitud: 18
```

**Notas importantes**: La concatenación crea nuevas strings; para muchas, usa table.concat.