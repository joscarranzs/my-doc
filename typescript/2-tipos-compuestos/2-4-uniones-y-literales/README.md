# Uniones y literales

Uniones permiten múltiples tipos, literales restringen a valores específicos.

## Uniones

`Tipo1 | Tipo2`

**Ejemplo de la vida real**: ID que puede ser string o number.

```typescript
function imprimirID(id: string | number) {
    console.log(`ID: ${id}`);
}

imprimirID("abc");
imprimirID(123);
```

## Literales

Valores específicos.

**Ejemplo de la vida real**: Direcciones de API.

```typescript
type MetodoHTTP = "GET" | "POST" | "PUT" | "DELETE";

function hacerRequest(metodo: MetodoHTTP, url: string) {
    // ...
}
```

**Notas importantes**: Uniones con type guards mejoran seguridad. Literales previenen valores inválidos.