# Indexed access types

Acceder a tipos de propiedades.

**Sintaxis**: `Tipo[Clave]`

**Ejemplo de la vida real**: Tipo de propiedad específica.

```typescript
interface APIResponse {
    data: {
        usuario: {
            nombre: string;
            email: string;
        };
    };
}

type NombreUsuario = APIResponse["data"]["usuario"]["nombre"]; // string
```

**Notas importantes**: Navega estructuras de tipos.