# Generators

Funciones que pueden pausar y reanudar ejecución.

Sintaxis: function* () { yield valor; }

**Ejemplo de la vida real**: Generando secuencia infinita.

```javascript
function* contador() {
    let i = 0;
    while (true) {
        yield i++;
    }
}

let gen = contador();
console.log(gen.next().value); // 0
console.log(gen.next().value); // 1
```