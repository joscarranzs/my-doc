# Creación y acceso a elementos

Las tables son la estructura de datos principal en Lua, actuando como arrays, diccionarios u objetos.

## Creación de tables

Se crean con {} y pueden contener cualquier tipo de dato.

**Ejemplo de la vida real**: Representando un personaje en un juego.

```lua
local personaje = {
    nombre = "Heroe",
    vida = 100,
    inventario = {"espada", "escudo"}
}
```

## Acceso a elementos

Usa [] para índices numéricos o . para claves string.

**Ejemplo de la vida real**: Accediendo a propiedades de un producto.

```lua
local producto = {nombre = "Libro", precio = 20}
print(producto.nombre)      -- "Libro"
print(producto["precio"])   -- 20

-- Arrays
local colores = {"rojo", "azul", "verde"}
print(colores[1])  -- "rojo" (índices empiezan en 1)
```

**Notas importantes**: Las tables son referencias, no copias. Modificar una afecta todas las referencias.