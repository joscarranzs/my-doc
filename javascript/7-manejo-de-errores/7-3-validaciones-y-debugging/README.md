# Validaciones y debugging

Validar datos y usar herramientas de debugging.

- Validaciones: Comprobar tipos y valores.
- Debugging: console.log, debugger, DevTools.

**Ejemplo de la vida real**: Validando formulario antes de enviar.

```javascript
function validarEmail(email) {
    if (!email.includes("@")) {
        throw new Error("Email inválido");
    }
}

console.log("Debug: Iniciando validación");
try {
    validarEmail("usuario@dominio.com");
    console.log("Email válido");
} catch (error) {
    console.error("Error:", error.message);
}
```