# HTML5 APIs (Geolocation, Local Storage, etc.)

APIs modernas para funcionalidad avanzada.

## Geolocation

Obtener ubicación del usuario.

**Ejemplo**:

```javascript
if (navigator.geolocation) {
    navigator.geolocation.getCurrentPosition(function(position) {
        console.log(position.coords.latitude, position.coords.longitude);
    });
}
```

## Local Storage

Almacenamiento persistente.

**Ejemplo de la vida real**: Recordar preferencias.

```javascript
// Guardar
localStorage.setItem('tema', 'oscuro');

// Leer
const tema = localStorage.getItem('tema');
```

## Drag and Drop

Arrastrar elementos.

**Ejemplo**:

```html
(`<div id="dropzone" ondrop="drop(event)" ondragover="allowDrop(event)">`)
    Suelta archivos aquí
(`</div>`)
```

**Notas importantes**: Pedir permisos apropiadamente. Manejar errores de soporte.