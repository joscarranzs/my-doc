# Async/await

Sintaxis para trabajar con promesas de forma síncrona.

- async: Marca función asíncrona.
- await: Espera resolución de promesa.

**Ejemplo de la vida real**: Función para login.

```javascript
async function login(email, password) {
    try {
        let response = await fetch("/login", {
            method: "POST",
            body: JSON.stringify({ email, password })
        });
        let data = await response.json();
        console.log("Login exitoso", data);
    } catch (error) {
        console.error("Error en login", error);
    }
}
```