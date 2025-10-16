# Atributos de multimedia (controls, autoplay, loop, muted)

Controlan comportamiento de audio/video.

## controls

Muestra controles de reproducción.

**Ejemplo**:

```html
(video controls)
    (source src="video.mp4" type="video/mp4")
(/video)
```

## autoplay

Reproduce automáticamente (con restricciones).

**Ejemplo**:

```html
(audio autoplay muted)
    (source src="musica.mp3" type="audio/mpeg")
(/audio)
```

**Nota**: Autoplay requiere muted en la mayoría de navegadores.

## loop

Repite indefinidamente.

**Ejemplo de la vida real**: Música de fondo.

```html
(audio loop)
    (source src="ambient.mp3" type="audio/mpeg")
(/audio)
```

## muted

Silencia por defecto.

**Notas importantes**: Usar autoplay con precaución. Respeta preferencias del usuario.