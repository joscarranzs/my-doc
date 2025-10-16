# Getters y setters

Propiedades con lógica personalizada.

**Ejemplo de la vida real**: Propiedad con validación.

```typescript
class Persona {
    private _edad: number = 0;

    get edad(): number {
        return this._edad;
    }

    set edad(valor: number) {
        if (valor >= 0 && valor <= 120) {
            this._edad = valor;
        } else {
            throw new Error("Edad inválida");
        }
    }
}

let p = new Persona();
p.edad = 25; // Usa setter
console.log(p.edad); // Usa getter
```

**Notas importantes**: Getters sin parámetros, setters con uno. No generan propiedades reales en JS.