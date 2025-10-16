# Quiz interactivo

Preguntas con opciones múltiples.

## HTML

```html
(`<div class="quiz">`)
    (`<div id="pregunta-container">`)
        (`<h2 id="pregunta-texto">`)¿Cuál es la capital de Francia?(`</h2>`)
        (`<div class="opciones">`)
            (`<button class="opcion" data-correcta="false">`)Londres(`</button>`)
            (`<button class="opcion" data-correcta="false">`)Madrid(`</button>`)
            (`<button class="opcion" data-correcta="true">`)París(`</button>`)
            (`<button class="opcion" data-correcta="false">`)Roma(`</button>`)
        (`</div>`)
    (`</div>`)
    
    (`<div id="resultado" style="display: none;">`)
        (`<h2>`)Resultado(`</h2>`)
        (`<p id="puntuacion">`)Puntuación: 0/10(`</p>`)
        (`<button id="reiniciar">`)Reiniciar Quiz(`</button>`)
    (`</div>`)
(`</div>`)
```

## JavaScript

```javascript
const preguntas = [
    {
        pregunta: "¿Cuál es la capital de Francia?",
        opciones: ["Londres", "Madrid", "París", "Roma"],
        correcta: 2
    },
    // Más preguntas...
];

let preguntaActual = 0;
let puntuacion = 0;

function mostrarPregunta() {
    const pregunta = preguntas[preguntaActual];
    document.getElementById('pregunta-texto').textContent = pregunta.pregunta;
    
    const botones = document.querySelectorAll('.opcion');
    botones.forEach((boton, index) => {
        boton.textContent = pregunta.opciones[index];
        boton.onclick = () => seleccionarOpcion(index);
    });
}

function seleccionarOpcion(index) {
    if (index === preguntas[preguntaActual].correcta) {
        puntuacion++;
    }
    
    preguntaActual++;
    
    if (preguntaActual < preguntas.length) {
        mostrarPregunta();
    } else {
        mostrarResultado();
    }
}

function mostrarResultado() {
    document.getElementById('pregunta-container').style.display = 'none';
    document.getElementById('resultado').style.display = 'block';
    document.getElementById('puntuacion').textContent = `Puntuación: ${puntuacion}/${preguntas.length}`;
}

document.getElementById('reiniciar').addEventListener('click', () => {
    preguntaActual = 0;
    puntuacion = 0;
    document.getElementById('resultado').style.display = 'none';
    document.getElementById('pregunta-container').style.display = 'block';
    mostrarPregunta();
});

mostrarPregunta();
```

**Objetivo**: Practicar lógica, arrays, eventos.