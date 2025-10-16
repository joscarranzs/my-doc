# Multimedia ((`<audio>`), (`<video>`), (`<source>`), (`<track>`))

Incrustar audio y video.

## (`<video>`)

**Ejemplo de la vida real**: Video tutorial.

```html
(`<video controls width="640" height="360">`)
    (`<source src="tutorial.mp4" type="video/mp4">`)
    (`<source src="tutorial.webm" type="video/webm">`)
    Tu navegador no soporta video.
(`</video>`)
```

## (`<audio>`)

**Ejemplo de la vida real**: Podcast.

```html
(`<audio controls>`)
    (`<source src="podcast.mp3" type="audio/mpeg">`)
    (`<source src="podcast.ogg" type="audio/ogg">`)
    Tu navegador no soporta audio.
(`</audio>`)
```

## (`<track>`)

Subtítulos y descripciones.

**Ejemplo**:

```html
(`<video controls>`)
    (`<source src="video.mp4" type="video/mp4">`)
    (`<track kind="subtitles" src="subtitulos.vtt" srclang="es" label="Español">`)
(`</video>`)
```

**Notas importantes**: Proporcionar múltiples formatos para compatibilidad. Siempre incluir controles.