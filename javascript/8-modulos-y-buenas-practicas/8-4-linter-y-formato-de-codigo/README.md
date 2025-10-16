# Linter y formato de código (ESLint, Prettier)

Herramientas para calidad de código.

- ESLint: Detecta errores y estilo.
- Prettier: Formatea automáticamente.

**Ejemplo de la vida real**: Configuración en package.json.

```json
{
  "scripts": {
    "lint": "eslint src/",
    "format": "prettier --write src/"
  }
}
```

Asegura consistencia en equipo.