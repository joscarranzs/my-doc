# Métodos estáticos

Métodos que pertenecen a la clase, no a instancias. Se llaman con Class.metodo().

**Ejemplo de la vida real**: Función utilitaria en una clase.

```javascript
class Utilidades {
    static sumar(a, b) {
        return a + b;
    }
}

console.log(Utilidades.sumar(5, 3)); // 8
```