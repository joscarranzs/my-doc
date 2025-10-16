# Conversor de unidades

Convertir entre diferentes unidades de medida.

## HTML

```html
(div class="conversor-unidades")
    (h1)Conversor de Unidades(/h1)
    
    (div class="conversor")
        (select id="categoria")
            (option value="longitud")Longitud(/option)
            (option value="peso")Peso(/option)
            (option value="temperatura")Temperatura(/option)
            (option value="volumen")Volumen(/option)
        (/select)
        
        (div class="entrada")
            (input type="number" id="valor-entrada" placeholder="Valor")
            (select id="unidad-entrada")
                (!-- Se llena dinámicamente --)
            (/select)
        (/div)
        
        (div class="salida")
            (input type="number" id="valor-salida" readonly)
            (select id="unidad-salida")
                (!-- Se llena dinámicamente --)
            (/select)
        (/div)
    (/div)
    
    (button id="intercambiar")↔ Intercambiar(/button)
(/div)
```

## JavaScript

```javascript
const conversiones = {
    longitud: {
        metros: 1,
        kilometros: 1000,
        centimetros: 0.01,
        milimetros: 0.001,
        pulgadas: 0.0254,
        pies: 0.3048,
        yardas: 0.9144,
        millas: 1609.34
    },
    peso: {
        gramos: 1,
        kilogramos: 1000,
        libras: 453.592,
        onzas: 28.3495,
        toneladas: 1000000
    },
    temperatura: {
        celsius: 'C',
        fahrenheit: 'F',
        kelvin: 'K'
    },
    volumen: {
        litros: 1,
        mililitros: 0.001,
        metros_cubicos: 1000,
        galones_us: 3.78541,
        galones_uk: 4.54609,
        pintas_us: 0.473176,
        tazas: 0.236588
    }
};

function actualizarUnidades() {
    const categoria = document.getElementById('categoria').value;
    const unidades = Object.keys(conversiones[categoria]);
    
    const selectEntrada = document.getElementById('unidad-entrada');
    const selectSalida = document.getElementById('unidad-salida');
    
    selectEntrada.innerHTML = '';
    selectSalida.innerHTML = '';
    
    unidades.forEach(unidad => {
        const opcionEntrada = document.createElement('option');
        opcionEntrada.value = unidad;
        opcionEntrada.textContent = unidad.charAt(0).toUpperCase() + unidad.slice(1);
        selectEntrada.appendChild(opcionEntrada);
        
        const opcionSalida = document.createElement('option');
        opcionSalida.value = unidad;
        opcionSalida.textContent = unidad.charAt(0).toUpperCase() + unidad.slice(1);
        selectSalida.appendChild(opcionSalida);
    });
    
    // Establecer unidades por defecto
    if (categoria === 'longitud') {
        selectEntrada.value = 'metros';
        selectSalida.value = 'kilometros';
    } else if (categoria === 'peso') {
        selectEntrada.value = 'gramos';
        selectSalida.value = 'kilogramos';
    } else if (categoria === 'temperatura') {
        selectEntrada.value = 'celsius';
        selectSalida.value = 'fahrenheit';
    } else if (categoria === 'volumen') {
        selectEntrada.value = 'litros';
        selectSalida.value = 'mililitros';
    }
}

function convertir() {
    const categoria = document.getElementById('categoria').value;
    const valor = parseFloat(document.getElementById('valor-entrada').value);
    const unidadEntrada = document.getElementById('unidad-entrada').value;
    const unidadSalida = document.getElementById('unidad-salida').value;
    
    if (isNaN(valor)) {
        document.getElementById('valor-salida').value = '';
        return;
    }
    
    let resultado;
    
    if (categoria === 'temperatura') {
        resultado = convertirTemperatura(valor, unidadEntrada, unidadSalida);
    } else {
        const factorEntrada = conversiones[categoria][unidadEntrada];
        const factorSalida = conversiones[categoria][unidadSalida];
        resultado = (valor * factorEntrada) / factorSalida;
    }
    
    document.getElementById('valor-salida').value = resultado.toFixed(6);
}

function convertirTemperatura(valor, entrada, salida) {
    let celsius;
    
    // Convertir a Celsius primero
    if (entrada === 'celsius') {
        celsius = valor;
    } else if (entrada === 'fahrenheit') {
        celsius = (valor - 32) * 5/9;
    } else if (entrada === 'kelvin') {
        celsius = valor - 273.15;
    }
    
    // Convertir de Celsius a unidad de salida
    if (salida === 'celsius') {
        return celsius;
    } else if (salida === 'fahrenheit') {
        return (celsius * 9/5) + 32;
    } else if (salida === 'kelvin') {
        return celsius + 273.15;
    }
}

document.getElementById('categoria').addEventListener('change', actualizarUnidades);
document.getElementById('valor-entrada').addEventListener('input', convertir);
document.getElementById('unidad-entrada').addEventListener('change', convertir);
document.getElementById('unidad-salida').addEventListener('change', convertir);

document.getElementById('intercambiar').addEventListener('click', () => {
    const entrada = document.getElementById('unidad-entrada').value;
    const salida = document.getElementById('unidad-salida').value;
    const valorEntrada = document.getElementById('valor-entrada').value;
    const valorSalida = document.getElementById('valor-salida').value;
    
    document.getElementById('unidad-entrada').value = salida;
    document.getElementById('unidad-salida').value = entrada;
    document.getElementById('valor-entrada').value = valorSalida;
    document.getElementById('valor-salida').value = valorEntrada;
});

actualizarUnidades();
```

**Objetivo**: Practicar lógica matemática, objetos complejos, conversión de unidades.