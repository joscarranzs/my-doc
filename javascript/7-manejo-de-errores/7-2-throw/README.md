# throw

Lanza errores personalizados con throw.

**Ejemplo de la vida real**: Validando entrada de usuario.

```javascript
function validarEdad(edad) {
    if (edad < 18) {
        throw new Error("Debes ser mayor de 18");
    }
    return true;
}

try {
    validarEdad(15);
} catch (error) {
    console.log(error.message);
}
```