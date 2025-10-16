# Contenido embebido (embed, object, source, track)

## Explicación

- embed: Contenido embebido genérico.
- object: Objeto embebido.
- source: Fuente para media.
- track: Pistas de texto (subtítulos).

## Ejemplo básico

```html
<embed src="file.pdf" type="application/pdf">

<object data="movie.swf" type="application/x-shockwave-flash"></object>

<video>
    <source src="video.mp4" type="video/mp4">
    <track src="subtitles.vtt" kind="subtitles" srclang="es" label="Español">
</video>
```

## Ejemplo de la vida real

Para subtítulos en video.

```html
<video controls>
    <source src="lecture.mp4" type="video/mp4">
    <track kind="subtitles" src="lecture-subs.vtt" srclang="en" label="English" default>
</video>
```

## Notas importantes

- embed es obsoleto, usa iframe.
- track para accesibilidad.

## Mejores prácticas

- Usa formatos modernos.
- Proporciona fallbacks.