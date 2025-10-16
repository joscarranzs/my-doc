# Enums

Enums definen conjuntos de constantes con nombres.

## Sintaxis

```typescript
enum Color {
    Rojo,
    Verde,
    Azul
}
```

**Ejemplo de la vida real**: Estados de una orden.

```typescript
enum EstadoOrden {
    Pendiente,
    Procesando,
    Enviada,
    Entregada
}

let orden: EstadoOrden = EstadoOrden.Procesando;
console.log(orden); // 1 (índice)
```

## Enums con valores personalizados

```typescript
enum HttpStatus {
    OK = 200,
    NotFound = 404,
    InternalError = 500
}
```

**Notas importantes**: Por defecto numéricos, pero pueden ser strings. Mejoran legibilidad sobre números mágicos.