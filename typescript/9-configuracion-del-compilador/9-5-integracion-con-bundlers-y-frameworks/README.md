# Integración con bundlers y frameworks

TS con Webpack, Vite, React, etc.

**Ejemplo con React**:

```typescript
// tsconfig.json
{
    "compilerOptions": {
        "jsx": "react-jsx",
        "lib": ["DOM", "ES2020"]
    }
}
```

**Notas importantes**: Frameworks tienen presets TS.