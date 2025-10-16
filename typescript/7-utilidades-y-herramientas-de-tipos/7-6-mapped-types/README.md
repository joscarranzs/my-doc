# Mapped types

Crear tipos transformando propiedades.

**Sintaxis**: `{ [K in Claves]: Tipo }`

**Ejemplo de la vida real**: Hacer todas las propiedades opcionales.

```typescript
type Opcional<T> = {
    [K in keyof T]?: T[K];
};

interface Usuario {
    nombre: string;
    edad: number;
}

type UsuarioOpcional = Opcional<Usuario>; // { nombre?: string; edad?: number; }
```

**Notas importantes**: Base de utility types como Partial.