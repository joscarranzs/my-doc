# Funciones básicas

Las funciones en Lua son bloques de código reutilizables. Pueden tomar parámetros, devolver valores y tener scope local.

## Declaración y llamada

Las funciones se declaran con `function nombre(parametros)` y se llaman con `nombre(argumentos)`.

**Ejemplo de la vida real**: Una función para calcular el área de un círculo.

```lua
function areaCirculo(radio)
    return 3.14159 * radio * radio
end

local area = areaCirculo(5)
print("Área: " .. area)  -- Área: 78.53975
```

## Parámetros y retorno

Las funciones pueden tener múltiples parámetros y devolver uno o más valores usando return.

**Ejemplo de la vida real**: Función que valida y formatea un email.

```lua
function validarEmail(email)
    if string.find(email, "@") then
        return true, string.lower(email)
    else
        return false, email
    end
end

local valido, emailFormateado = validarEmail("Usuario@Ejemplo.COM")
if valido then
    print("Email válido: " .. emailFormateado)
end
```

## Scope y variables locales

Las variables locales en funciones no afectan el exterior. Usa local para evitar globals.

**Ejemplo de la vida real**: Función que procesa datos sin modificar variables globales.

```lua
local datosGlobales = "original"

function procesarDatos(datos)
    local datosLocales = datos .. " procesado"
    return datosLocales
end

print(procesarDatos(datosGlobales))  -- "original procesado"
print(datosGlobales)  -- "original", sin cambios
```

**Notas importantes**: Las funciones son closures, capturando variables del scope donde se definieron.