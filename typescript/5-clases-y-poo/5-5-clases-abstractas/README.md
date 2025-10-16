# Clases abstractas

Clases que no se instancian, sirven como base.

**Sintaxis**: `abstract class Nombre`

**Ejemplo de la vida real**: Framework de formas geométricas.

```typescript
abstract class Forma {
    abstract calcularArea(): number;

    describir(): string {
        return `Área: ${this.calcularArea()}`;
    }
}

class Circulo extends Forma {
    radio: number;

    constructor(radio: number) {
        super();
        this.radio = radio;
    }

    calcularArea(): number {
        return Math.PI * this.radio ** 2;
    }
}

// let forma = new Forma(); // Error
let circulo = new Circulo(5);
console.log(circulo.describir());
```

**Notas importantes**: Métodos abstractos deben implementarse en subclases.