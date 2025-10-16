# Interfaces y clases combinadas

Clases implementan interfaces.

**Ejemplo de la vida real**: Servicio de autenticación.

```typescript
interface Autenticable {
    login(credenciales: { usuario: string; password: string }): boolean;
    logout(): void;
}

class AuthService implements Autenticable {
    login(credenciales: { usuario: string; password: string }): boolean {
        // lógica
        return true;
    }

    logout(): void {
        // lógica
    }
}
```

**Notas importantes**: Clases pueden implementar múltiples interfaces. Interfaces definen contratos.