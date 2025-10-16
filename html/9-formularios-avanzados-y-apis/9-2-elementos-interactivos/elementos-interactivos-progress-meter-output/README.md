# Elementos interactivos (progress, meter, output)

## Explicación

- progress: Barra de progreso.
- meter: Medidor.
- output: Resultado de cálculo.

## Ejemplo básico

```html
<progress value="70" max="100"></progress>
<meter value="0.8" min="0" max="1">80%</meter>
<output name="result">0</output>
```

## Ejemplo de la vida real

En una calculadora.

```html
<form oninput="result.value = parseInt(a.value) + parseInt(b.value)">
    <input type="number" id="a" value="0"> +
    <input type="number" id="b" value="0"> =
    <output name="result" for="a b">0</output>
</form>
```

## Notas importantes

- progress para tareas en progreso.
- meter para valores en rango.

## Mejores prácticas

- Usa ARIA para accesibilidad.
- Actualiza dinámicamente.