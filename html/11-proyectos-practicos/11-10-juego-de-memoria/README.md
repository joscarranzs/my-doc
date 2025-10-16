# Juego de memoria

Encontrar pares de cartas.

## HTML

```html
(div class="juego-memoria")
    (h1)Juego de Memoria(/h1)
    (div id="tablero" class="tablero")
        (!-- Las cartas se generan con JavaScript --)
    (/div)
    (div class="info")
        (span id="movimientos")Movimientos: 0(/span)
        (span id="tiempo")Tiempo: 0s(/span)
    (/div)
    (button id="reiniciar")Nuevo Juego(/button)
(/div)
```

## JavaScript

```javascript
const simbolos = ['🐶', '🐱', '🐭', '🐹', '🐰', '🦊', '🐻', '🐼'];
const cartas = [...simbolos, ...simbolos]; // Duplicar para pares
let cartasVolteadas = [];
let movimientos = 0;
let tiempo = 0;
let temporizador;
let paresEncontrados = 0;

function barajarCartas() {
    return cartas.sort(() => Math.random() - 0.5);
}

function crearTablero() {
    const tablero = document.getElementById('tablero');
    tablero.innerHTML = '';
    const cartasBarajadas = barajarCartas();
    
    cartasBarajadas.forEach((simbolo, index) => {
        const carta = document.createElement('div');
        carta.className = 'carta';
        carta.dataset.simbolo = simbolo;
        carta.dataset.index = index;
        carta.addEventListener('click', voltearCarta);
        tablero.appendChild(carta);
    });
}

function voltearCarta() {
    if (cartasVolteadas.length < 2 && !this.classList.contains('volteada')) {
        this.classList.add('volteada');
        this.textContent = this.dataset.simbolo;
        cartasVolteadas.push(this);
        
        if (cartasVolteadas.length === 2) {
            movimientos++;
            document.getElementById('movimientos').textContent = `Movimientos: ${movimientos}`;
            
            setTimeout(verificarPareja, 1000);
        }
    }
}

function verificarPareja() {
    const [carta1, carta2] = cartasVolteadas;
    
    if (carta1.dataset.simbolo === carta2.dataset.simbolo) {
        carta1.classList.add('pareja');
        carta2.classList.add('pareja');
        paresEncontrados++;
        
        if (paresEncontrados === simbolos.length) {
            clearInterval(temporizador);
            setTimeout(() => alert(`¡Felicidades! Completaste el juego en ${movimientos} movimientos y ${tiempo} segundos.`), 500);
        }
    } else {
        carta1.classList.remove('volteada');
        carta2.classList.remove('volteada');
        carta1.textContent = '';
        carta2.textContent = '';
    }
    
    cartasVolteadas = [];
}

function iniciarTemporizador() {
    temporizador = setInterval(() => {
        tiempo++;
        document.getElementById('tiempo').textContent = `Tiempo: ${tiempo}s`;
    }, 1000);
}

function reiniciarJuego() {
    clearInterval(temporizador);
    movimientos = 0;
    tiempo = 0;
    paresEncontrados = 0;
    cartasVolteadas = [];
    document.getElementById('movimientos').textContent = 'Movimientos: 0';
    document.getElementById('tiempo').textContent = 'Tiempo: 0s';
    crearTablero();
    iniciarTemporizador();
}

document.getElementById('reiniciar').addEventListener('click', reiniciarJuego);

reiniciarJuego();
```

**Objetivo**: Practicar algoritmos, estado complejo, temporizadores.