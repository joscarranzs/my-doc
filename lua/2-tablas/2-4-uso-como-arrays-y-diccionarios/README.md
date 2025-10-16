# Uso como arrays y diccionarios

Las tables sirven como arrays (índices numéricos) o diccionarios (claves arbitrarias).

## Como arrays

Índices empiezan en 1, útiles para listas ordenadas.

**Ejemplo de la vida real**: Lista de tareas diarias.

```lua
local tareas = {"desayunar", "trabajar", "cenar"}
print("Primera tarea: " .. tareas[1])
tareas[4] = "dormir"  -- Agrega al final
```

## Como diccionarios

Claves pueden ser strings, números o incluso tables.

**Ejemplo de la vida real**: Configuración de aplicación.

```lua
local config = {
    ["tema"] = "oscuro",
    [42] = "respuesta",
    [{x=1, y=2}] = "punto"  -- Clave table
}
print(config.tema)  -- "oscuro"
```

**Notas importantes**: Mezclar tipos puede ser confuso; usa convenciones claras. Las tables son dinámicas y flexibles.