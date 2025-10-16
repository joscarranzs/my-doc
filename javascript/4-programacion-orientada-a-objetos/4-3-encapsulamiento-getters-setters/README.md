# Encapsulamiento (getters/setters)

Getters y setters controlan el acceso a propiedades privadas.

**Ejemplo de la vida real**: Validando edad en un setter.

```javascript
class Persona {
    constructor() {
        this._edad = 0;
    }
    get edad() {
        return this._edad;
    }
    set edad(valor) {
        if (valor > 0) this._edad = valor;
    }
}

let p = new Persona();
p.edad = 25;
console.log(p.edad); // 25
p.edad = -5; // No cambia
```