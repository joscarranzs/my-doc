# Callbacks y problemas del "callback hell"

Callbacks anidados pueden hacer el código difícil de leer.

**Ejemplo de la vida real**: Cargando datos en secuencia.

```javascript
// Callback hell
cargarUsuario(id, function(usuario) {
    cargarPosts(usuario.id, function(posts) {
        mostrarPosts(posts, function() {
            console.log("Listo");
        });
    });
});

// Mejor con promesas
```

Usa promesas o async/await para evitarlo.