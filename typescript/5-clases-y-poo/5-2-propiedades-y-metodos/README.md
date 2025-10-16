# Propiedades y métodos

Clases tienen propiedades y métodos tipados.

**Ejemplo de la vida real**: Clase de producto.

```typescript
class Producto {
    nombre: string;
    precio: number;

    constructor(nombre: string, precio: number) {
        this.nombre = nombre;
        this.precio = precio;
    }

    calcularIVA(tasa: number = 0.16): number {
        return this.precio * tasa;
    }

    toString(): string {
        return `${this.nombre}: $${this.precio}`;
    }
}

let prod = new Producto("Libro", 20);
console.log(prod.toString()); // "Libro: $20"
```

**Notas importantes**: Constructor es opcional. Métodos pueden ser estáticos con `static`.