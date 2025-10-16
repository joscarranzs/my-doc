# Clases y modificadores (public, private, protected)

Clases en TS con modificadores de acceso.

**Sintaxis**:

```typescript
class Nombre {
    public propiedad: Tipo;
    private metodo() {}
    protected propiedadHeredada: Tipo;
}
```

**Ejemplo de la vida real**: Clase de cuenta bancaria.

```typescript
class Cuenta {
    private saldo: number = 0;

    public depositar(cantidad: number): void {
        this.saldo += cantidad;
    }

    protected obtenerSaldo(): number {
        return this.saldo;
    }
}

class CuentaPremium extends Cuenta {
    public retirar(cantidad: number): boolean {
        if (this.obtenerSaldo() >= cantidad) { // Accede a protected
            // lógica
            return true;
        }
        return false;
    }
}
```

**Notas importantes**: `public` por defecto. `private` solo en clase. `protected` en subclases.