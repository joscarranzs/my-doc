# Herencia y superclases

Clases heredan con `extends` y llaman super().

**Ejemplo de la vida real**: Jerarquía de vehículos.

```typescript
class Vehiculo {
    marca: string;

    constructor(marca: string) {
        this.marca = marca;
    }

    acelerar(): void {
        console.log("Acelerando");
    }
}

class Auto extends Vehiculo {
    modelo: string;

    constructor(marca: string, modelo: string) {
        super(marca); // Llama constructor padre
        this.modelo = modelo;
    }

    acelerar(): void {
        super.acelerar(); // Llama método padre
        console.log("Auto acelerando");
    }
}
```

**Notas importantes**: Solo herencia simple. `super` para acceder a padre.