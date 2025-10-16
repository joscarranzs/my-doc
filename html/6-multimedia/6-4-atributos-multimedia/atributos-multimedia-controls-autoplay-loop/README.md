# Atributos multimedia (controls, autoplay, loop)

## Explicación

- controls: Muestra controles.
- autoplay: Reproduce automáticamente.
- loop: Repite al terminar.

## Ejemplo básico

```html
<audio src="music.mp3" controls autoplay loop></audio>
```

## Ejemplo de la vida real

En un video de fondo.

```html
<video autoplay loop muted>
    <source src="background.mp4" type="video/mp4">
</video>
```

## Notas importantes

- autoplay puede ser bloqueado por navegadores.
- Usa muted con autoplay.

## Mejores prácticas

- No abuses de autoplay.
- Proporciona controles de usuario.