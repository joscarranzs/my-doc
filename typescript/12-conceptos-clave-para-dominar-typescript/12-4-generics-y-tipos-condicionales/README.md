# Generics y tipos condicionales

Combinar para tipos poderosos.

**Ejemplo de la vida real**: Utility type personalizado.

```typescript
type EsFuncion<T> = T extends (...args: any[]) => any ? T : never;
```

**Notas importantes**: Base de advanced patterns.