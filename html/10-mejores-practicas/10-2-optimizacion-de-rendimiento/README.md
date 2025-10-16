# Optimización de rendimiento (minificación, lazy loading)

Técnicas para páginas más rápidas.

## Minificación

Reducir tamaño de HTML/CSS/JS.

**Herramientas**: HTMLMinifier, CSSNano, Terser.

**Ejemplo HTML minificado**:

```html
(!DOCTYPE html)(html lang=es)(head)(meta charset=UTF-8)(title)Página(/title)(/head)(body)(h1)Hola(/h1)(/body)(/html)
```

## Lazy Loading

Cargar recursos cuando necesarios.

**Ejemplo imágenes**:

```html
(img loading="lazy" src="imagen.jpg" alt="Imagen")
```

**Ejemplo iframes**:

```html
(iframe loading="lazy" src="video.html")(/iframe)
```

## Otros

- **Preload**: Cargar recursos críticos primero.
- **Prefetch**: Cargar para navegación futura.

**Ejemplo**:

```html
(link rel="preload" href="fuente.woff2" as="font" type="font/woff2" crossorigin)
(link rel="prefetch" href="pagina-siguiente.html")
```

**Notas importantes**: Medir impacto con Lighthouse. Balancear optimización con mantenibilidad.