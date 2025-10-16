# Control de flujo

El control de flujo en Lua permite ejecutar código condicionalmente o repetidamente. Incluye condicionales para decisiones y bucles para iteraciones, esenciales para lógica programática.

## Condicionales (if, elseif, else)

Las estructuras if evalúan expresiones booleanas y ejecutan bloques de código basados en el resultado. elseif permite múltiples condiciones, y else maneja el caso por defecto.

**Sintaxis básica:**
```lua
if condición then
    -- código
elseif otra_condición then
    -- código
else
    -- código
end
```

**Ejemplo de la vida real**: Verificando permisos de usuario en una aplicación.

```lua
local usuario = "admin"
local edad = 25

if usuario == "admin" then
    print("Acceso total")
elseif edad >= 18 then
    print("Acceso limitado")
else
    print("Acceso denegado")
end
```

**Notas importantes**: Las condiciones pueden ser cualquier expresión que evalúe a boolean o nil (falso). Usa paréntesis opcionalmente para claridad.

## Bucles (while, repeat...until, for)

Los bucles repiten código hasta que una condición se cumpla.

- **while**: Ejecuta mientras la condición sea true.
- **repeat...until**: Ejecuta al menos una vez, luego hasta que la condición sea true.
- **for**: Para rangos numéricos o iteradores.

**Ejemplo de la vida real**: Procesando una lista de tareas pendientes.

```lua
local tareas = {"Comprar leche", "Llamar al doctor", "Estudiar Lua"}
local i = 1

while i <= #tareas do
    print("Tarea " .. i .. ": " .. tareas[i])
    i = i + 1
end

-- Usando for
for j = 1, #tareas do
    print("Procesando: " .. tareas[j])
end

-- repeat until
local contador = 0
repeat
    contador = contador + 1
    print("Intento " .. contador)
until contador >= 3
```

**Notas importantes**: El bucle for numérico es eficiente. Para tables, usa pairs/ipairs. Evita bucles infinitos verificando condiciones.