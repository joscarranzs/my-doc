# Herencia (extends, super)

La herencia permite que una clase herede propiedades y métodos de otra.

- extends: Crea subclase.
- super(): Llama al constructor padre.

**Ejemplo de la vida real**: Clases para empleados y gerentes.

```javascript
class Empleado {
    constructor(nombre, salario) {
        this.nombre = nombre;
        this.salario = salario;
    }
}

class Gerente extends Empleado {
    constructor(nombre, salario, departamento) {
        super(nombre, salario);
        this.departamento = departamento;
    }
}

let gerente = new Gerente("Juan", 5000, "Ventas");
```