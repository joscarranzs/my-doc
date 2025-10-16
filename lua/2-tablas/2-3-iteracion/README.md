# Iteración (pairs, ipairs)

Para recorrer tables, usa pairs (todos los elementos) o ipairs (índices numéricos secuenciales).

## pairs

Itera sobre todas las claves y valores, incluyendo no numéricas.

**Ejemplo de la vida real**: Mostrando propiedades de un objeto.

```lua
local persona = {nombre = "Ana", edad = 30, ciudad = "Madrid"}
for clave, valor in pairs(persona) do
    print(clave .. ": " .. tostring(valor))
end
-- Output: nombre: Ana, edad: 30, ciudad: Madrid
```

## ipairs

Itera solo índices numéricos desde 1 hasta el primer nil.

**Ejemplo de la vida real**: Procesando una lista ordenada.

```lua
local frutas = {"manzana", "pera", "uva"}
for i, fruta in ipairs(frutas) do
    print(i .. ". " .. fruta)
end
-- Output: 1. manzana, 2. pera, 3. uva
```

**Notas importantes**: pairs es para diccionarios, ipairs para arrays. El orden en pairs no está garantizado.