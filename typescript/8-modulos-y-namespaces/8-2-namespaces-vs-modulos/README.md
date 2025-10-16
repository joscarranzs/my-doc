# Namespaces vs módulos

Namespaces agrupan código globalmente, módulos son archivos separados.

**Ejemplo de la vida real**: Namespace para utilidades.

```typescript
// math.ts
namespace MathUtils {
    export function sumar(a: number, b: number): number {
        return a + b;
    }
}

// Uso
MathUtils.sumar(1, 2);
```

**Notas importantes**: Namespaces para compatibilidad, módulos preferidos en proyectos modernos.