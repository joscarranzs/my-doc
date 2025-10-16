# Opciones clave (strict, noImplicitAny, target, module)

Opciones importantes en tsconfig.

- **strict**: Habilita checks estrictos.
- **noImplicitAny**: Error en tipos implícitos any.
- **target**: Versión JS objetivo (ES5, ES2020).
- **module**: Sistema de módulos (commonjs, es2020).

**Ejemplo de la vida real**: Config para app moderna.

```json
{
    "compilerOptions": {
        "strict": true,
        "noImplicitAny": true,
        "target": "ES2020",
        "module": "ES2020"
    }
}
```

**Notas importantes**: Strict recomendado para nuevos proyectos.