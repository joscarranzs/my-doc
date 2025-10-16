# Video (video)

## Explicación

Incrusta contenido de video.

## Ejemplo básico

```html
<video src="video.mp4" controls></video>
```

## Ejemplo de la vida real

En un sitio de streaming.

```html
<video controls width="640" height="360">
    <source src="movie.mp4" type="video/mp4">
    <source src="movie.webm" type="video/webm">
    Tu navegador no soporta video.
</video>
```

## Notas importantes

- Múltiples formatos para compatibilidad.
- Especifica dimensiones.

## Mejores prácticas

- Usa poster para thumbnail.
- Considera accesibilidad con captions.