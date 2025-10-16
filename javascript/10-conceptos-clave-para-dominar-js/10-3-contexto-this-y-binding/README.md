# Contexto (this) y binding

'this' depende del contexto de llamada.

- En método: objeto.
- En función: window/global.
- En arrow: contexto padre.

**Ejemplo de la vida real**: Callback perdiendo 'this'.

```javascript
let obj = {
    valor: 42,
    metodo: function() {
        setTimeout(function() {
            console.log(this.valor); // undefined
        }, 100);
    }
};
obj.metodo();
```