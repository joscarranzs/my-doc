# Utility types (Partial, Pick, Omit, Readonly, Record, ReturnType, Required)

Tipos predefinidos para transformaciones comunes.

**Ejemplos de la vida real**:

```typescript
interface Usuario {
    nombre: string;
    edad: number;
    email: string;
}

type UsuarioParcial = Partial<Usuario>; // Todas opcionales
type UsuarioSeleccionado = Pick<Usuario, "nombre" | "email">; // Solo algunas
type UsuarioSinEmail = Omit<Usuario, "email">; // Excluir
type UsuarioSoloLectura = Readonly<Usuario>; // Inmutable
type Config = Record<string, boolean>; // { [key: string]: boolean }
type RetornoFuncion = ReturnType<() => string>; // string
type UsuarioRequerido = Required<Usuario>; // Todas requeridas
```

**Notas importantes**: Simplifican código de tipos. Importados de "typescript".