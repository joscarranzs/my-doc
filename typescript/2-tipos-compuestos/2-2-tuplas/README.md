# Tuplas

Tuplas son arrays con tipos fijos en posiciones específicas.

**Sintaxis**: `[Tipo1, Tipo2, ...]`

**Ejemplo de la vida real**: Coordenadas o pares clave-valor.

```typescript
let coordenada: [number, number] = [10, 20];
let persona: [string, number] = ["Ana", 25];

console.log(coordenada[0]); // 10
```

## Tuplas con etiquetas

Usar interfaces para claridad.

```typescript
interface Punto {
    0: number;
    1: number;
    length: 2;
}

let punto: Punto = [5, 10];
```

**Notas importantes**: Acceso por índice, no por nombre. Útil para datos estructurados fijos.