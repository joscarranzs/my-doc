# Tipos especiales

TS añade tipos para casos especiales donde los primitivos no bastan.

## any

Desactiva el tipado, permite cualquier valor. Usar con cuidado.

**Ejemplo de la vida real**: Integración con librerías no tipadas.

```typescript
let datoExterno: any = JSON.parse('{"nombre": "Ana"}');
console.log(datoExterno.nombre); // Acceso dinámico
```

## unknown

Similar a any, pero más seguro: requiere type checking antes de usar.

**Ejemplo de la vida real**: Datos de APIs externas.

```typescript
let respuestaAPI: unknown = fetchData();
if (typeof respuestaAPI === "string") {
    console.log(respuestaAPI.toUpperCase());
}
```

## never

Para funciones que nunca retornan (lanzan error o loops infinitos).

**Ejemplo de la vida real**: Función que siempre lanza error.

```typescript
function errorFatal(mensaje: string): never {
    throw new Error(mensaje);
}
```

## void

Para funciones sin retorno explícito.

**Ejemplo de la vida real**: Event handlers.

```typescript
function logMensaje(): void {
    console.log("Mensaje logged");
}
```

**Notas importantes**: Evitar `any` en código nuevo. `unknown` es preferible para datos no confiables.