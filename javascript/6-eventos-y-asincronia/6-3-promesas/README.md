# Promesas

Las promesas representan operaciones asíncronas que pueden resolverse o rechazarse.

- then(): Maneja resolución.
- catch(): Maneja error.
- finally(): Siempre ejecuta.

**Ejemplo de la vida real**: Obteniendo datos de una API.

```javascript
fetch("https://api.example.com/data")
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error(error))
    .finally(() => console.log("Operación completa"));
```

Encadenamiento evita callback hell.