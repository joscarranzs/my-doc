# Intersecciones

Combinan múltiples tipos en uno.

**Sintaxis**: `Tipo1 & Tipo2`

**Ejemplo de la vida real**: Objeto que combina propiedades.

```typescript
interface Nombre {
    nombre: string;
}

interface Edad {
    edad: number;
}

type Persona = Nombre & Edad;

let p: Persona = { nombre: "Ana", edad: 25 };
```

**Notas importantes**: Todas las propiedades deben estar presentes. Útil para mixins o extensiones.