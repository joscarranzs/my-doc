# Progressive Enhancement y Graceful Degradation

Estrategias para compatibilidad.

## Progressive Enhancement

Empezar con funcionalidad básica, añadir avanzada.

**Ejemplo**: Formulario con validación.

```html
(`<form action="/submit">`)
    (`<input type="email" name="email" required>`)
    (`<button type="submit">`)Enviar(`</button>`)
(`</form>`)
(`<script>`)
    // Añadir validación JS si disponible
    if (document.querySelector) {
        // Código de validación avanzada
    }
(`</script>`)
```

## Graceful Degradation

Funcionalidad completa, degradar elegantemente.

**Ejemplo**: Aplicación con WebGL.

```html
(`<canvas id="grafico">`)(`</canvas>`)
(`<script>`)
    const canvas = document.getElementById('grafico');
    if (canvas.getContext) {
        // WebGL o Canvas
    } else {
        // Fallback: tabla o imagen estática
        canvas.style.display = 'none';
        document.getElementById('fallback').style.display = 'block';
    }
(`</script>`)
```

**Notas importantes**: Probar en navegadores objetivo. Usar feature detection, no browser detection.