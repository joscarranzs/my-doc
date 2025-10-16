# print y io.write

print muestra en consola con newline, io.write sin newline.

**Ejemplo de la vida real**: Mostrando progreso.

```lua
print("Procesando...")  -- Con newline
io.write("Progreso: ")
for i = 1, 10 do
    io.write(".")  -- Sin newline
end
print()  -- Newline final
```

**Notas importantes**: print convierte a string automáticamente.