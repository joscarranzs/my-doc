# Tipado estático vs dinámico

El tipado estático de TS verifica tipos en compile-time, mientras que JS usa tipado dinámico en runtime.

## Ventajas del tipado estático

- **Detección temprana de errores**: Bugs se capturan antes de ejecutar.
- **Mejor IDE support**: Autocompletado, refactoring seguro.
- **Documentación viva**: Los tipos sirven como documentación.
- **Performance**: Optimizaciones posibles en compilación.

**Ejemplo de la vida real**: En una API REST, asegurar que los datos enviados tengan el tipo correcto.

```typescript
interface Usuario {
    id: number;
    nombre: string;
    email: string;
}

function crearUsuario(datos: Usuario): Usuario {
    // TS asegura que datos tenga id, nombre, email
    return datos;
}

// Error: falta 'email'
crearUsuario({ id: 1, nombre: "Ana" }); // Compile error
```

## Comparación con tipado dinámico

- **JS**: Flexible pero propenso a errores runtime.
- **TS**: Menos flexible pero más seguro.

**Notas importantes**: TS permite `any` para gradual adoption. El equilibrio entre seguridad y flexibilidad depende del proyecto.