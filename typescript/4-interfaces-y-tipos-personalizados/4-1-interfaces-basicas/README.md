# Interfaces básicas

Interfaces definen contratos para objetos.

**Sintaxis**:

```typescript
interface Nombre {
    propiedad: Tipo;
    metodo(): TipoRetorno;
}
```

**Ejemplo de la vida real**: API de usuario.

```typescript
interface UsuarioAPI {
    id: number;
    nombre: string;
    obtenerPerfil(): Promise<Perfil>;
}

class UsuarioImpl implements UsuarioAPI {
    id: number;
    nombre: string;

    constructor(id: number, nombre: string) {
        this.id = id;
        this.nombre = nombre;
    }

    obtenerPerfil(): Promise<Perfil> {
        return fetch(`/usuarios/${this.id}`).then(r => r.json());
    }
}
```

**Notas importantes**: Interfaces no generan código JS, solo para type checking.