# HTML5 moderno y APIs nativas

## Explicación

Usar características modernas de HTML5 y APIs del navegador.

## Ejemplo básico

```html
<input type="color">
<input type="datetime-local">
<canvas id="canvas"></canvas>
<script>
    navigator.geolocation.getCurrentPosition(pos => {
        console.log(pos.coords);
    });
</script>
```

## Ejemplo de la vida real

En una app web.

```html
<video controls>
    <source src="video.mp4" type="video/mp4">
</video>
<button onclick="share()">Compartir</button>
<script>
    async function share() {
        if (navigator.share) {
            await navigator.share({ title: 'Mi video', url: window.location.href });
        }
    }
</script>
```

## Notas importantes

- Verificar soporte con feature detection.
- Fallbacks para navegadores antiguos.

## Mejores prácticas

- Progressive enhancement.
- APIs con permisos del usuario.