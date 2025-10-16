# Generador de contraseñas

Crear contraseñas seguras con opciones personalizables.

## HTML

```html
(div class="generador-contrasenas")
    (h1)Generador de Contraseñas(/h1)
    
    (div class="opciones")
        (label)
            (input type="checkbox" id="mayusculas" checked) Mayúsculas (A-Z)
        (/label)
        (label)
            (input type="checkbox" id="minusculas" checked) Minúsculas (a-z)
        (/label)
        (label)
            (input type="checkbox" id="numeros" checked) Números (0-9)
        (/label)
        (label)
            (input type="checkbox" id="simbolos") Símbolos (!@#$%)
        (/label)
    (/div)
    
    (div class="longitud")
        (label for="longitud")Longitud: (span id="valor-longitud")12(/span)(/label)
        (input type="range" id="longitud" min="4" max="32" value="12")
    (/div)
    
    (button id="generar")Generar Contraseña(/button)
    
    (div class="resultado")
        (input type="text" id="contrasena" readonly)
        (button id="copiar")Copiar(/button)
    (/div)
    
    (div class="seguridad")
        (div class="barra-fuerza")
            (div id="barra" class="barra")(/div)
        (/div)
        (span id="texto-fuerza")Fuerza: Débil(/span)
    (/div)
(/div)
```

## JavaScript

```javascript
function generarContrasena() {
    const mayusculas = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
    const minusculas = 'abcdefghijklmnopqrstuvwxyz';
    const numeros = '0123456789';
    const simbolos = '!@#$%^&*()_+-=[]{}|;:,.()?';
    
    let caracteres = '';
    if (document.getElementById('mayusculas').checked) caracteres += mayusculas;
    if (document.getElementById('minusculas').checked) caracteres += minusculas;
    if (document.getElementById('numeros').checked) caracteres += numeros;
    if (document.getElementById('simbolos').checked) caracteres += simbolos;
    
    if (caracteres === '') {
        alert('Selecciona al menos un tipo de carácter');
        return;
    }
    
    const longitud = document.getElementById('longitud').value;
    let contrasena = '';
    
    for (let i = 0; i < longitud; i++) {
        contrasena += caracteres.charAt(Math.floor(Math.random() * caracteres.length));
    }
    
    document.getElementById('contrasena').value = contrasena;
    evaluarFuerza(contrasena);
}

function evaluarFuerza(contrasena) {
    let puntuacion = 0;
    
    // Longitud
    if (contrasena.length >= 8) puntuacion += 1;
    if (contrasena.length >= 12) puntuacion += 1;
    
    // Variedad de caracteres
    if (/[a-z]/.test(contrasena)) puntuacion += 1;
    if (/[A-Z]/.test(contrasena)) puntuacion += 1;
    if (/[0-9]/.test(contrasena)) puntuacion += 1;
    if (/[^a-zA-Z0-9]/.test(contrasena)) puntuacion += 1;
    
    const barra = document.getElementById('barra');
    const texto = document.getElementById('texto-fuerza');
    
    barra.className = 'barra';
    
    if (puntuacion <= 2) {
        barra.classList.add('debil');
        texto.textContent = 'Fuerza: Débil';
    } else if (puntuacion <= 4) {
        barra.classList.add('media');
        texto.textContent = 'Fuerza: Media';
    } else {
        barra.classList.add('fuerte');
        texto.textContent = 'Fuerza: Fuerte';
    }
    
    barra.style.width = `${(puntuacion / 6) * 100}%`;
}

document.getElementById('generar').addEventListener('click', generarContrasena);

document.getElementById('longitud').addEventListener('input', function() {
    document.getElementById('valor-longitud').textContent = this.value;
});

document.getElementById('copiar').addEventListener('click', async () => {
    const contrasena = document.getElementById('contrasena').value;
    try {
        await navigator.clipboard.writeText(contrasena);
        alert('Contraseña copiada al portapapeles');
    } catch (err) {
        // Fallback para navegadores antiguos
        const input = document.getElementById('contrasena');
        input.select();
        document.execCommand('copy');
        alert('Contraseña copiada al portapapeles');
    }
});

// Generar contraseña inicial
generarContrasena();
```

**Objetivo**: Practicar algoritmos, validación, APIs modernas.