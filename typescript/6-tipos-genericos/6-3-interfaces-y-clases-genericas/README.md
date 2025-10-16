# Interfaces y clases genéricas

Interfaces y clases con tipos genéricos.

**Ejemplo de la vida real**: Contenedor genérico.

```typescript
interface Contenedor<T> {
    valor: T;
    obtener(): T;
}

class Caja<T> implements Contenedor<T> {
    valor: T;

    constructor(valor: T) {
        this.valor = valor;
    }

    obtener(): T {
        return this.valor;
    }
}

let cajaString = new Caja<string>("Hola");
```

**Notas importantes**: Útil para librerías reutilizables.