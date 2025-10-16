# Extensión de interfaces

Interfaces pueden extender otras.

**Sintaxis**: `interface Hija extends Padre`

**Ejemplo de la vida real**: Jerarquía de empleados.

```typescript
interface Persona {
    nombre: string;
    edad: number;
}

interface Empleado extends Persona {
    salario: number;
    departamento: string;
}

let emp: Empleado = {
    nombre: "Ana",
    edad: 30,
    salario: 50000,
    departamento: "IT"
};
```

**Notas importantes**: Herencia múltiple con extends Interface1, Interface2.