# Principios SOLID y DRY

Principios para código limpio.

- SOLID: Single responsibility, Open-closed, etc.
- DRY: Don't Repeat Yourself.

**Ejemplo de la vida real**: Función reutilizable en lugar de código duplicado.

```javascript
// DRY: Una función para validar
function esEmailValido(email) {
    return email.includes("@");
}

// En lugar de repetir la lógica en múltiples lugares
```

Mejora mantenibilidad.