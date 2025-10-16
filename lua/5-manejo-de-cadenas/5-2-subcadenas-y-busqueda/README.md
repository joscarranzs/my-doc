# Subcadenas y búsqueda

string.sub extrae subcadenas, string.find busca patrones.

**Ejemplo de la vida real**: Extrayendo dominio de email.

```lua
local email = "usuario@ejemplo.com"
local arroba = string.find(email, "@")
if arroba then
    local dominio = string.sub(email, arroba + 1)
    print("Dominio: " .. dominio)  -- "ejemplo.com"
end
```

**Notas importantes**: Los índices empiezan en 1. string.find devuelve posiciones.