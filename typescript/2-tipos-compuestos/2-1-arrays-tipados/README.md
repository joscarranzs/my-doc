# Arrays tipados

Arrays en TS se tipan con `Tipo[]` o `Array<Tipo>`.

## Sintaxis básica

```typescript
let numeros: number[] = [1, 2, 3];
let strings: Array<string> = ["a", "b"];
```

## Métodos tipados

Métodos como push, map mantienen tipos.

**Ejemplo de la vida real**: Lista de productos en carrito.

```typescript
interface Producto {
    nombre: string;
    precio: number;
}

let carrito: Producto[] = [];
carrito.push({ nombre: "Libro", precio: 20 });
carrito.map(p => p.precio).forEach(precio => console.log(precio));
```

## Arrays readonly

Para arrays inmutables.

```typescript
let readonlyArray: readonly number[] = [1, 2, 3];
// readonlyArray.push(4); // Error
```

**Notas importantes**: Usar `readonly` para prevenir mutaciones accidentales.