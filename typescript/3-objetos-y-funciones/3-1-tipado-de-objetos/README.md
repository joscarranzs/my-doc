# Tipado de objetos

Objetos se tipan con interfaces o tipos inline.

**Ejemplo de la vida real**: Usuario en app.

```typescript
interface Usuario {
    id: number;
    nombre: string;
    email?: string; // Opcional
}

let usuario: Usuario = {
    id: 1,
    nombre: "Ana"
};
```

## Propiedades opcionales y readonly

```typescript
interface Config {
    readonly version: string;
    debug?: boolean;
}

let config: Config = { version: "1.0" };
// config.version = "2.0"; // Error
```

**Notas importantes**: Interfaces describen contratos. Usar readonly para inmutabilidad.