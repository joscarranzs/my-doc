# Encapsulamiento básico

El encapsulamiento se simula con closures o convenciones de nomenclatura.

**Ejemplo de la vida real**: Propiedad privada con closure.

```lua
function crearCuenta(saldoInicial)
    local saldo = saldoInicial  -- Privado
    return {
        depositar = function(cantidad)
            saldo = saldo + cantidad
        end,
        retirar = function(cantidad)
            if cantidad <= saldo then
                saldo = saldo - cantidad
                return true
            end
            return false
        end,
        getSaldo = function()
            return saldo
        end
    }
end

local cuenta = crearCuenta(100)
cuenta:depositar(50)
print(cuenta:getSaldo())  -- 150
```

**Notas importantes**: Lua no tiene modificadores de acceso; usa convenciones como _privado.