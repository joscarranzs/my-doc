# Diseño de tipos reutilizables

Crear tipos que se reutilicen.

**Ejemplo de la vida real**: API responses.

```typescript
type APIResponse<T> = {
    data: T;
    error?: string;
};

type UserResponse = APIResponse<{ id: number; name: string }>;
```

**Notas importantes**: Mejora consistencia.