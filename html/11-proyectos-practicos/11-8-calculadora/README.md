# Calculadora

Operaciones matemáticas básicas.

## HTML

```html
<div class="calculadora">
    <input type="text" id="pantalla" readonly>
    <div class="botones">
        <button class="numero">7</button>
        <button class="numero">8</button>
        <button class="numero">9</button>
        <button class="operador">+</button>
        
        <button class="numero">4</button>
        <button class="numero">5</button>
        <button class="numero">6</button>
        <button class="operador">-</button>
        
        <button class="numero">1</button>
        <button class="numero">2</button>
        <button class="numero">3</button>
        <button class="operador">*</button>
        
        <button class="numero">0</button>
        <button class="igual">=</button>
        <button class="limpiar">C</button>
        <button class="operador">/</button>
    </div>
</div>
```

## JavaScript

```javascript
let pantalla = document.getElementById('pantalla');
let operacion = '';
let numeroAnterior = '';
let operandoActual = false;

document.querySelectorAll('.numero').forEach(boton => {
    boton.addEventListener('click', () => {
        if (operandoActual) {
            pantalla.value = '';
            operandoActual = false;
        }
        pantalla.value += boton.textContent;
    });
});

document.querySelectorAll('.operador').forEach(boton => {
    boton.addEventListener('click', () => {
        if (pantalla.value !== '') {
            numeroAnterior = pantalla.value;
            operacion = boton.textContent;
            operandoActual = true;
        }
    });
});

document.querySelector('.igual').addEventListener('click', () => {
    if (numeroAnterior !== '' && pantalla.value !== '') {
        let resultado;
        const num1 = parseFloat(numeroAnterior);
        const num2 = parseFloat(pantalla.value);
        
        switch (operacion) {
            case '+': resultado = num1 + num2; break;
            case '-': resultado = num1 - num2; break;
            case '*': resultado = num1 * num2; break;
            case '/': resultado = num1 / num2; break;
        }
        
        pantalla.value = resultado;
        numeroAnterior = '';
        operandoActual = true;
    }
});

document.querySelector('.limpiar').addEventListener('click', () => {
    pantalla.value = '';
    numeroAnterior = '';
    operacion = '';
});
```

**Objetivo**: Practicar lógica matemática, eventos, estado.