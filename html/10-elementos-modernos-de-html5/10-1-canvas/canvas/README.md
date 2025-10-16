# Canvas

## Explicación

Elemento para dibujar gráficos 2D con JavaScript.

## Ejemplo básico

```html
<canvas id="myCanvas" width="200" height="100"></canvas>
<script>
    const canvas = document.getElementById('myCanvas');
    const ctx = canvas.getContext('2d');
    ctx.fillStyle = 'red';
    ctx.fillRect(10, 10, 50, 50);
</script>
```

## Ejemplo de la vida real

En un gráfico simple.

```html
<canvas id="chart" width="400" height="200"></canvas>
<script>
    // Código para dibujar gráfico de barras
</script>
```

## Notas importantes

- Requiere JavaScript.
- No accesible por defecto.

## Mejores prácticas

- Proporciona fallback.
- Usa para gráficos dinámicos.