# Iframes (<iframe>)

Incrustar contenido externo.

**Sintaxis**:

```html
<iframe src="https://ejemplo.com" width="600" height="400" title="Contenido embebido"></iframe>
```

**Ejemplo de la vida real**: Video de YouTube.

```html
<iframe src="https://www.youtube.com/embed/VIDEO_ID" 
        width="560" height="315" 
        title="Video tutorial"
        allowfullscreen></iframe>
```

**Atributos importantes**:
- **src**: URL del contenido.
- **title**: Descripción para accesibilidad.
- **width/height**: Dimensiones.

**Notas importantes**: Precaución con seguridad (XSS). Usar sandbox para contenido no confiable.