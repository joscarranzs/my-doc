# Inferencia y anotación de tipos

TS infiere tipos automáticamente, pero permite anotaciones explícitas.

## Inferencia automática

TS deduce tipos de asignaciones iniciales.

**Ejemplo de la vida real**: Variables locales.

```typescript
let mensaje = "Hola"; // Inferido como string
let contador = 0; // number
contador = "texto"; // Error: no se puede asignar string a number
```

## Anotación explícita

Usar cuando la inferencia no es suficiente.

**Ejemplo de la vida real**: Parámetros de función.

```typescript
function saludar(nombre: string, edad?: number): string {
    return `Hola ${nombre}${edad ? `, tienes ${edad} años` : ""}`;
}

saludar("Ana", 25); // OK
saludar("Ana"); // OK, edad opcional
```

## Best practices

- Dejar inferir cuando es obvio.
- Anotar en APIs públicas y casos complejos.

**Notas importantes**: La inferencia reduce boilerplate, pero anotaciones mejoran claridad en equipos.