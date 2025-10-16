# Pattern matching (simulado)

Simular pattern matching con tipos.

**Ejemplo de la vida real**: Procesar formas.

```typescript
type Forma = { tipo: "circulo"; radio: number } | { tipo: "rectangulo"; ancho: number; alto: number };

function area(forma: Forma): number {
    switch (forma.tipo) {
        case "circulo":
            return Math.PI * forma.radio ** 2;
        case "rectangulo":
            return forma.ancho * forma.alto;
    }
}
```

**Notas importantes**: Exhaustive checking asegura cubrir todos los casos.