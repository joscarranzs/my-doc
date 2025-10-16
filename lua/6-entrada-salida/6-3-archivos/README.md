# Archivos (io.open, :read, :write, :close)

Para archivos, abre con io.open, lee/escribe con métodos del handle.

**Ejemplo de la vida real**: Leyendo un archivo de configuración.

```lua
local archivo = io.open("config.txt", "r")
if archivo then
    local contenido = archivo:read("*a")  -- Lee todo
    print(contenido)
    archivo:close()
else
    print("No se pudo abrir el archivo")
end
```

**Notas importantes**: Siempre cierra archivos. Modos: "r" leer, "w" escribir.