# Audio (audio)

## Explicación

Incrusta contenido de audio.

## Ejemplo básico

```html
<audio src="audio.mp3" controls></audio>
```

## Ejemplo de la vida real

En un reproductor de podcast.

```html
<audio controls>
    <source src="podcast.mp3" type="audio/mpeg">
    <source src="podcast.ogg" type="audio/ogg">
    Tu navegador no soporta audio.
</audio>
```

## Notas importantes

- Usa múltiples sources para compatibilidad.
- controls muestra controles.

## Mejores prácticas

- Proporciona alternativas.
- Optimiza archivos.