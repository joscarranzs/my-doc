# keyof, typeof, typeof keyof

Operadores para tipos dinámicos.

**Ejemplo de la vida real**: Extraer claves de objeto.

```typescript
interface Usuario {
    nombre: string;
    edad: number;
}

type ClavesUsuario = keyof Usuario; // "nombre" | "edad"

let config = { tema: "oscuro" };
type Tema = typeof config.tema; // string

type ClavesConfig = keyof typeof config; // "tema"
```

**Notas importantes**: Útil para APIs genéricas.