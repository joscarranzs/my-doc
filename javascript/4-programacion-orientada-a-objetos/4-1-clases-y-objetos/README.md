# Clases y objetos

Las clases son plantillas para crear objetos con propiedades y métodos.

Sintaxis: class Nombre { constructor() {} metodo() {} }

**Ejemplo de la vida real**: Modelando usuarios en una app.

```javascript
class Usuario {
    constructor(nombre, edad) {
        this.nombre = nombre;
        this.edad = edad;
    }
    presentarse() {
        console.log(`Soy ${this.nombre}, tengo ${this.edad} años`);
    }
}

let ana = new Usuario("Ana", 25);
ana.presentarse();
```