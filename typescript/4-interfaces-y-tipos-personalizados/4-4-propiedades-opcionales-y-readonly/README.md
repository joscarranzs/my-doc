# Propiedades opcionales y readonly

Propiedades pueden ser opcionales o inmutables.

**Ejemplo de la vida real**: Configuración de app.

```typescript
interface Config {
    readonly version: string;
    debug?: boolean;
    tema?: "claro" | "oscuro";
}

let config: Config = { version: "1.0", debug: true };
// config.version = "2.0"; // Error
```

**Notas importantes**: `?` para opcionales. `readonly` previene mutaciones.