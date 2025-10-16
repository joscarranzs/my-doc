# Tabla de datos interactiva

Mostrar datos en tabla con funcionalidades.

## HTML de tabla

```html
(table id="tabla-usuarios")
    (thead)
        (tr)
            (th)Nombre(/th)
            (th)Email(/th)
            (th)Rol(/th)
            (th)Acciones(/th)
        (/tr)
    (/thead)
    (tbody)
        (tr)
            (td)Juan Pérez(/td)
            (td)juan@email.com(/td)
            (td)Admin(/td)
            (td)
                (button class="editar")Editar(/button)
                (button class="eliminar")Eliminar(/button)
            (/td)
        (/tr)
        (!-- Más filas --)
    (/tbody)
(/table)
```

## Funcionalidad de búsqueda

```html
(input type="text" id="busqueda" placeholder="Buscar usuarios...")
```

```javascript
document.getElementById('busqueda').addEventListener('input', function() {
    const filtro = this.value.toLowerCase();
    const filas = document.querySelectorAll('#tabla-usuarios tbody tr');
    
    filas.forEach(fila => {
        const texto = fila.textContent.toLowerCase();
        fila.style.display = texto.includes(filtro) ? '' : 'none';
    });
});
```

## Ordenamiento

```javascript
document.querySelectorAll('th').forEach(header => {
    header.addEventListener('click', () => {
        // Lógica de ordenamiento
    });
});
```

**Objetivo**: Practicar tablas, manipulación DOM, eventos.