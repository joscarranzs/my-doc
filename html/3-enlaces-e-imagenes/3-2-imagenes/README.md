# Imágenes (`(img)`)

Incrustar imágenes en la página.

**Sintaxis**:

```html
(img src="ruta/imagen.jpg" alt="Descripción")
```

**Ejemplo de la vida real**: Galería de fotos.

```html
(figure)
    (img src="foto.jpg" alt="Paisaje montañoso" width="300" height="200")
    (figcaption)Un hermoso paisaje(/figcaption)
(/figure)
```

**Atributos importantes**:
- **src**: Ruta de la imagen.
- **alt**: Texto alternativo.
- **width/height**: Dimensiones.

**Notas importantes**: Siempre incluir alt para accesibilidad. Optimizar imágenes para web.