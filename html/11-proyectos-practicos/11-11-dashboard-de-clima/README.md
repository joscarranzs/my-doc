# Dashboard de clima

Mostrar información meteorológica.

## HTML

```html
(`<div class="dashboard-clima">`)
    (`<h1>`)Clima Actual(`</h1>`)
    (`<div class="busqueda">`)
        (`<input type="text" id="ciudad-input" placeholder="Ingresa una ciudad">`)
        (`<button id="buscar">`)Buscar(`</button>`)
    (`</div>`)
    
    (`<div id="info-clima" style="display: none;">`)
        (`<h2 id="ciudad">`)(`</h2>`)
        (`<div class="temperatura">`)
            (`<span id="temp">`)(`</span>`)
            (`<span id="descripcion">`)(`</span>`)
        (`</div>`)
        (`<div class="detalles">`)
            (`<div>`)Humedad: (`<span id="humedad">`)(`</span>`)(`</div>`)
            (`<div>`)Viento: (`<span id="viento">`)(`</span>`)(`</div>`)
            (`<div>`)Presión: (`<span id="presion">`)(`</span>`)(`</div>`)
        (`</div>`)
    (`</div>`)
    
    (`<div id="error" style="display: none;">`)(`</div>`)
(`</div>`)
```

## JavaScript (usando OpenWeatherMap API)

```javascript
const apiKey = 'TU_API_KEY_AQUI'; // Obtén una API key gratuita en openweathermap.org

document.getElementById('buscar').addEventListener('click', () => {
    const ciudad = document.getElementById('ciudad-input').value;
    if (ciudad) {
        obtenerClima(ciudad);
    }
});

async function obtenerClima(ciudad) {
    try {
        const respuesta = await fetch(`https://api.openweathermap.org/data/2.5/weather?q=${ciudad}&appid=${apiKey}&units=metric&lang=es`);
        
        if (!respuesta.ok) {
            throw new Error('Ciudad no encontrada');
        }
        
        const datos = await respuesta.json();
        mostrarClima(datos);
    } catch (error) {
        mostrarError(error.message);
    }
}

function mostrarClima(datos) {
    document.getElementById('error').style.display = 'none';
    const infoClima = document.getElementById('info-clima');
    infoClima.style.display = 'block';
    
    document.getElementById('ciudad').textContent = `${datos.name}, ${datos.sys.country}`;
    document.getElementById('temp').textContent = `${Math.round(datos.main.temp)}°C`;
    document.getElementById('descripcion').textContent = datos.weather[0].description;
    document.getElementById('humedad').textContent = `${datos.main.humidity}%`;
    document.getElementById('viento').textContent = `${datos.wind.speed} m/s`;
    document.getElementById('presion').textContent = `${datos.main.pressure} hPa`;
}

function mostrarError(mensaje) {
    document.getElementById('info-clima').style.display = 'none';
    const errorDiv = document.getElementById('error');
    errorDiv.textContent = mensaje;
    errorDiv.style.display = 'block';
}

// Obtener clima de ubicación actual
if (navigator.geolocation) {
    navigator.geolocation.getCurrentPosition(async (position) => {
        try {
            const respuesta = await fetch(`https://api.openweathermap.org/data/2.5/weather?lat=${position.coords.latitude}&lon=${position.coords.longitude}&appid=${apiKey}&units=metric&lang=es`);
            const datos = await respuesta.json();
            mostrarClima(datos);
        } catch (error) {
            console.log('Error obteniendo clima por geolocalización');
        }
    });
}
```

**Objetivo**: Practicar APIs, async/await, manejo de errores.