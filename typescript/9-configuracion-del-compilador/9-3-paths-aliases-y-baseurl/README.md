# Paths, aliases y baseUrl

Configurar rutas de import.

**Ejemplo**:

```json
{
    "compilerOptions": {
        "baseUrl": "./src",
        "paths": {
            "@components/*": ["components/*"],
            "@utils/*": ["utils/*"]
        }
    }
}
```

**Notas importantes**: Mejora mantenibilidad en proyectos grandes.