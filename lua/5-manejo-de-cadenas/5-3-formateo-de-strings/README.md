# Formateo de strings

string.format crea strings formateadas, similar a printf.

**Ejemplo de la vida real**: Formateando precios.

```lua
local precio = 19.99
local nombre = "Libro"
local descripcion = string.format("Producto: %s, Precio: $%.2f", nombre, precio)
print(descripcion)  -- "Producto: Libro, Precio: $19.99"
```

**Notas importantes**: Usa %s para strings, %d para enteros, %f para floats.