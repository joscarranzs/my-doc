# Métodos importantes (table.insert, table.remove, table.concat)

La librería table proporciona funciones útiles para manipular arrays.

## table.insert

Agrega elementos a una table.

**Ejemplo de la vida real**: Agregando items a un carrito de compras.

```lua
local carrito = {"manzana", "pan"}
table.insert(carrito, "leche")  -- Agrega al final
table.insert(carrito, 1, "jugo")  -- Inserta en posición 1
print(table.concat(carrito, ", "))  -- "jugo, manzana, pan, leche"
```

## table.remove

Elimina elementos.

**Ejemplo de la vida real**: Removiendo tareas completadas.

```lua
local tareas = {"lavar", "cocinar", "estudiar"}
table.remove(tareas, 2)  -- Remueve "cocinar"
print(table.concat(tareas, ", "))  -- "lavar, estudiar"
```

## table.concat

Une elementos en un string.

**Ejemplo de la vida real**: Generando una lista de nombres.

```lua
local nombres = {"Ana", "Juan", "María"}
local lista = table.concat(nombres, "; ")
print(lista)  -- "Ana; Juan; María"
```

**Notas importantes**: Estas funciones modifican la table original. Para strings grandes, concat es eficiente.