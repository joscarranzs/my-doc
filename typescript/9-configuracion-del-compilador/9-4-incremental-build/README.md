# Incremental build

Compilación incremental para velocidad.

**Config**:

```json
{
    "compilerOptions": {
        "incremental": true,
        "tsBuildInfoFile": ".tsbuildinfo"
    }
}
```

**Notas importantes**: Solo recompila cambios. Útil en desarrollo.