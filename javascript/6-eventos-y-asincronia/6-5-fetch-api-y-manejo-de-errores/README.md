# Fetch API y manejo de errores

Fetch realiza peticiones HTTP. Maneja respuestas y errores.

**Ejemplo de la vida real**: Cargando productos de una tienda.

```javascript
fetch("https://api.tienda.com/productos")
    .then(response => {
        if (!response.ok) throw new Error("Error HTTP");
        return response.json();
    })
    .then(productos => {
        productos.forEach(p => console.log(p.nombre));
    })
    .catch(error => console.error("Error:", error));
```

Usa try/catch con async/await.