# Estructura de tsconfig

Archivo de configuración del compilador.

**Ejemplo básico**:

```json
{
    "compilerOptions": {
        "target": "ES2020",
        "module": "commonjs",
        "strict": true,
        "outDir": "./dist"
    },
    "include": ["src/**/*"],
    "exclude": ["node_modules"]
}
```

**Notas importantes**: Controla cómo TS compila. `tsc --init` crea uno.