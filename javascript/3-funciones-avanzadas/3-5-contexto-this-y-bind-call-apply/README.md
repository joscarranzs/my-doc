# Contexto (this) y bind/call/apply

'this' refiere al objeto que ejecuta la función. Puede cambiar según el contexto.

- call(): Llama función con 'this' específico.
- apply(): Similar a call, pero argumentos como array.
- bind(): Crea nueva función con 'this' fijo.

**Ejemplo de la vida real**: Método de objeto usado en callback.

```javascript
let usuario = {
    nombre: "Ana",
    saludar: function() {
        console.log("Hola " + this.nombre);
    }
};

setTimeout(usuario.saludar.bind(usuario), 1000); // "Hola Ana"
```