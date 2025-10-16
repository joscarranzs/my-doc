# Reproductor de video personalizado

Controles personalizados para video HTML5.

## HTML

```html
(div class="reproductor-video")
    (video id="mi-video" poster="poster.jpg")
        (source src="video.mp4" type="video/mp4")
        Tu navegador no soporta video.
    (/video)
    
    (div class="controles")
        (button id="play-pause")Play(/button)
        (input type="range" id="barra-progreso" min="0" max="100" value="0")
        (span id="tiempo")0:00 / 0:00(/span)
        (button id="mute")Mute(/button)
        (input type="range" id="volumen" min="0" max="1" step="0.1" value="1")
        (button id="fullscreen")Fullscreen(/button)
    (/div)
(/div)
```

## JavaScript para controles

```javascript
const video = document.getElementById('mi-video');
const playPauseBtn = document.getElementById('play-pause');

playPauseBtn.addEventListener('click', () => {
    if (video.paused) {
        video.play();
        playPauseBtn.textContent = 'Pause';
    } else {
        video.pause();
        playPauseBtn.textContent = 'Play';
    }
});

// Más event listeners para otros controles...
```

## Mejoras

- Subtítulos.
- Velocidad de reproducción.
- Lista de reproducción.

**Objetivo**: Practicar multimedia, eventos, manipulación DOM.