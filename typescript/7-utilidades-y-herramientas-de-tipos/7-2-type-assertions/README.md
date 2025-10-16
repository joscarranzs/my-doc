# Type assertions (as)

Forzar un tipo cuando se sabe mejor que TS.

**Sintaxis**: `valor as Tipo`

**Ejemplo de la vida real**: Acceder a propiedades específicas.

```typescript
let elemento = document.getElementById("miDiv") as HTMLDivElement;
elemento.style.color = "red";
```

**Notas importantes**: Usar con cuidado, puede causar runtime errors. Preferir type guards.