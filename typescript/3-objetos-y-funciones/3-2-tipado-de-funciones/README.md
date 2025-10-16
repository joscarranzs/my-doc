# Tipado de funciones

Funciones se tipan en parámetros y retorno.

## Parámetros y retorno

```typescript
function sumar(a: number, b: number): number {
    return a + b;
}
```

## Funciones opcionales y predeterminadas

```typescript
function saludar(nombre: string, saludo?: string): string {
    return `${saludo || "Hola"} ${nombre}`;
}

function multiplicar(a: number, b: number = 1): number {
    return a * b;
}
```

**Ejemplo de la vida real**: API de cálculo.

```typescript
type Operacion = (a: number, b: number) => number;

let operaciones: { [key: string]: Operacion } = {
    sumar: (a, b) => a + b,
    restar: (a, b) => a - b
};
```

**Notas importantes**: Parámetros opcionales van al final. Usar tipos de función para callbacks.