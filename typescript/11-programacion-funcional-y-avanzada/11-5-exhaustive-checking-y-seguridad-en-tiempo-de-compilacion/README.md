# Exhaustive checking y seguridad en tiempo de compilación

Asegurar que todos los casos estén manejados.

**Ejemplo de la vida real**: Estados de máquina.

```typescript
type Estado = "idle" | "loading" | "success" | "error";

function manejarEstado(estado: Estado) {
    switch (estado) {
        case "idle":
            return "Esperando";
        case "loading":
            return "Cargando";
        case "success":
            return "Éxito";
        case "error":
            return "Error";
        default:
            const _exhaustive: never = estado; // Error si falta caso
            return _exhaustive;
    }
}
```

**Notas importantes**: `never` fuerza exhaustividad.