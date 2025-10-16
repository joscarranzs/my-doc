# Funciones flecha

Las funciones flecha son una sintaxis concisa introducida en ES6, especialmente útiles para funciones anónimas y callbacks.

Sintaxis: (parametros) => { cuerpo }

**Ejemplo de la vida real**: Filtrando productos baratos en una tienda online.

```javascript
let productos = [10, 50, 100];
let baratos = productos.filter(precio => precio < 50);
console.log(baratos); // [10]
```

No tienen su propio 'this', heredan del contexto padre.