# Compatibilidad y migración progresiva

Estrategias para migrar a TS.

**Técnicas**:

- Usar `// @ts-ignore` temporalmente.
- Configurar `allowJs: true`.
- Migrar archivos uno por uno.

**Ejemplo de la vida real**: Proyecto híbrido.

```json
// tsconfig.json
{
    "allowJs": true,
    "checkJs": false
}
```

**Notas importantes**: Migración puede ser gradual.