# Sobrecarga de funciones

Múltiples firmas para una función.

**Ejemplo de la vida real**: Función que acepta string o number.

```typescript
function combinar(a: string, b: string): string;
function combinar(a: number, b: number): number;
function combinar(a: any, b: any): any {
    return a + b;
}

console.log(combinar("Hola", " Mundo")); // "Hola Mundo"
console.log(combinar(1, 2)); // 3
```

**Notas importantes**: Implementación debe manejar todas las sobrecargas. Útil para APIs flexibles.