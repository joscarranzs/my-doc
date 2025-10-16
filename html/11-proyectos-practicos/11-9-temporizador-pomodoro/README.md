# Temporizador/Pomodoro

Contador con intervalos de trabajo y descanso.

## HTML

```html
(div class="pomodoro")
    (h1)Pomodoro Timer(/h1)
    (div id="tiempo-restante")25:00(/div)
    (div class="controles")
        (button id="iniciar")Iniciar(/button)
        (button id="pausar")Pausar(/button)
        (button id="reiniciar")Reiniciar(/button)
    (/div)
    (div class="modos")
        (button id="trabajo" class="activo")Trabajo (25min)(/button)
        (button id="descanso")Descanso (5min)(/button)
    (/div)
    (div id="estado")Listo para trabajar(/div)
(/div)
```

## JavaScript

```javascript
let tiempoRestante = 25 * 60; // 25 minutos en segundos
let temporizador;
let modoTrabajo = true;

function actualizarDisplay() {
    const minutos = Math.floor(tiempoRestante / 60);
    const segundos = tiempoRestante % 60;
    document.getElementById('tiempo-restante').textContent = 
        `${minutos.toString().padStart(2, '0')}:${segundos.toString().padStart(2, '0')}`;
}

function iniciarTemporizador() {
    temporizador = setInterval(() => {
        tiempoRestante--;
        actualizarDisplay();
        
        if (tiempoRestante <= 0) {
            clearInterval(temporizador);
            cambiarModo();
            reproducirSonido();
        }
    }, 1000);
}

function pausarTemporizador() {
    clearInterval(temporizador);
}

function reiniciarTemporizador() {
    clearInterval(temporizador);
    tiempoRestante = modoTrabajo ? 25 * 60 : 5 * 60;
    actualizarDisplay();
}

function cambiarModo() {
    modoTrabajo = !modoTrabajo;
    tiempoRestante = modoTrabajo ? 25 * 60 : 5 * 60;
    
    document.getElementById('trabajo').classList.toggle('activo');
    document.getElementById('descanso').classList.toggle('activo');
    
    document.getElementById('estado').textContent = 
        modoTrabajo ? '¡Tiempo de trabajar!' : '¡Toma un descanso!';
    
    actualizarDisplay();
}

function reproducirSonido() {
    // Reproducir sonido de notificación
    const audio = new Audio('notificacion.mp3');
    audio.play();
}

// Event listeners
document.getElementById('iniciar').addEventListener('click', iniciarTemporizador);
document.getElementById('pausar').addEventListener('click', pausarTemporizador);
document.getElementById('reiniciar').addEventListener('click', reiniciarTemporizador);
document.getElementById('trabajo').addEventListener('click', () => {
    if (!modoTrabajo) cambiarModo();
});
document.getElementById('descanso').addEventListener('click', () => {
    if (modoTrabajo) cambiarModo();
});

actualizarDisplay();
```

**Objetivo**: Practicar temporizadores, estado, UX.