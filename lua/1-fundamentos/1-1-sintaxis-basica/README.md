# Sintaxis básica

Esta sección introduce los elementos fundamentales de la sintaxis de Lua, incluyendo cómo declarar y usar variables, los tipos de datos disponibles, operadores para realizar operaciones, y cómo agregar comentarios al código. Lua es un lenguaje de scripting ligero y eficiente, conocido por su simplicidad y flexibilidad, especialmente en el desarrollo de juegos y aplicaciones embebidas.

## Variables (local, global)

En Lua, las variables no necesitan ser declaradas explícitamente; se crean al asignarles un valor. Sin embargo, se recomienda usar `local` para variables locales, que tienen un scope limitado al bloque donde se definen, mejorando la performance y evitando conflictos de nombres. Las variables globales, sin `local`, están disponibles en todo el programa pero pueden causar problemas en código modular.

**Diferencias clave:**
- **Local**: Más eficiente, no poluciona el espacio global, esencial en funciones y bucles.
- **Global**: Accesible desde cualquier parte, pero puede llevar a bugs si no se maneja con cuidado.

**Ejemplo de la vida real**: En un script de un juego, usar variables locales para el puntaje de un nivel específico, evitando que interfiera con otros niveles.

```lua
local puntaje = 100  -- Variable local, solo visible aquí
globalConfig = "Configuración general"  -- Variable global

function calcularBonus()
    local bonus = puntaje * 0.1  -- Accede a la local del scope superior
    return bonus
end

print(calcularBonus())  -- 10
print(puntaje)  -- 100, accesible aquí
```

**Notas importantes**: Siempre usa `local` a menos que necesites compartir datos globalmente. En Lua 5.1+, las variables no inicializadas son `nil`.

## Tipos de datos (nil, boolean, number, string, table, function, userdata, thread)

Lua tiene 8 tipos de datos básicos, todos dinámicos. No hay declaraciones de tipo; el tipo se determina en runtime.

- **nil**: Representa la ausencia de valor, similar a null en otros lenguajes.
- **boolean**: true o false.
- **number**: Números de punto flotante (no hay enteros separados en versiones antiguas).
- **string**: Cadenas de texto, inmutables.
- **table**: Estructuras de datos versátiles, usadas como arrays, diccionarios, objetos.
- **function**: Funciones como valores de primera clase.
- **userdata**: Datos binarios de C, usados en extensiones.
- **thread**: Para corutinas.

**Ejemplo de la vida real**: En una aplicación de inventario, usar tables para representar productos con diferentes tipos de datos.

```lua
local producto = {
    nombre = "Laptop",  -- string
    precio = 999.99,    -- number
    disponible = true,  -- boolean
    descripcion = nil   -- nil, aún no asignada
}

print(type(producto.nombre))  -- string
print(type(producto))         -- table
```

**Notas importantes**: Usa `type()` para verificar tipos. Las tables son el corazón de Lua; casi todo se construye con ellas.

## Operadores (aritméticos, lógicos, relacionales, concatenación)

Lua soporta operadores estándar para matemáticas, lógica y comparación.

- **Aritméticos**: +, -, *, /, %, ^ (potencia), - (negativo).
- **Relacionales**: ==, ~= (no igual), <, >, <=, >=.
- **Lógicos**: and, or, not.
- **Concatenación**: .. (une strings).

**Ejemplo de la vida real**: Calculando descuentos en una tienda virtual.

```lua
local precio = 100
local descuento = 0.2
local precioFinal = precio * (1 - descuento)  -- 80

local mensaje = "El precio final es $" .. tostring(precioFinal)  -- Concatenación

if precioFinal < 50 and descuento > 0.1 then
    print("Oferta especial: " .. mensaje)
end
```

**Notas importantes**: La concatenación con .. puede ser ineficiente para muchas operaciones; considera table.concat para strings grandes. Los operadores lógicos devuelven el último valor evaluado, no boolean.

## Comentarios

Los comentarios en Lua se hacen con -- para línea o --[[ ]] para bloque. Son ignorados por el intérprete.

**Ejemplo de la vida real**: Documentando un script de configuración.

```lua
-- Este es un comentario de línea
local config = "valor"

--[[
Comentario de bloque
Útil para documentación extensa
]]
```

**Notas importantes**: Usa comentarios para explicar lógica compleja, especialmente en código que otros leerán.