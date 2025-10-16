# Tipos primitivos

TS incluye los tipos primitivos de JS más bigint, con anotaciones estrictas.

## Tipos disponibles

- **string**: Cadenas de texto.
- **number**: Números (no diferencia entre int/float).
- **boolean**: true/false.
- **null**: Valor nulo explícito.
- **undefined**: Valor no definido.
- **symbol**: Valores únicos (ES6).
- **bigint**: Números enteros grandes.

**Ejemplo de la vida real**: Modelar datos de un formulario de registro.

```typescript
let nombre: string = "Juan";
let edad: number = 25;
let esActivo: boolean = true;
let ultimaConexion: Date | null = null; // Unión con null
let idUnico: symbol = Symbol("usuario");
let saldoGrande: bigint = 1000000000000n;
```

## Uso en funciones y variables

Anotar tipos previene asignaciones incorrectas.

**Ejemplo de la vida real**: Función de validación.

```typescript
function validarEmail(email: string): boolean {
    return email.includes("@");
}

let emailUsuario: string = "usuario@dominio.com";
if (validarEmail(emailUsuario)) {
    console.log("Email válido");
}
```

**Notas importantes**: Usar tipos específicos mejora la legibilidad. `bigint` para números muy grandes, pero no compatible con operadores normales.