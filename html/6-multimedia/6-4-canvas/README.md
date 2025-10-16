# Canvas ((`<canvas>`))

Superficie de dibujo para gráficos 2D/3D con JavaScript.

**Ejemplo básico**:

```html
(`<canvas id="miCanvas" width="400" height="300">`)(`</canvas>`)
(`<script>`)
const canvas = document.getElementById('miCanvas');
const ctx = canvas.getContext('2d');
ctx.fillStyle = 'red';
ctx.fillRect(10, 10, 100, 100);
(`</script>`)
```

**Ejemplo de la vida real**: Gráfico interactivo.

```html
(`<canvas id="grafico" width="600" height="400">`)(`</canvas>`)
(`<!-- JavaScript para dibujar gráfico de barras -->`)
```

**Usos comunes**:
- Juegos.
- Visualizaciones de datos.
- Edición de imágenes.
- Generación de gráficos.

**Notas importantes**: Requiere JavaScript. No accesible por defecto, usar fallback.