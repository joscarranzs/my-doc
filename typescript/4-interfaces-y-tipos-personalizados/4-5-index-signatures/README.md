# Index signatures

Permiten objetos con claves dinámicas.

**Sintaxis**: `[key: Tipo]: TipoValor`

**Ejemplo de la vida real**: Diccionario de traducciones.

```typescript
interface Traducciones {
    [idioma: string]: string;
}

let trad: Traducciones = {
    "es": "Hola",
    "en": "Hello"
};
```

**Notas importantes**: Todas las propiedades deben coincidir con el tipo del índice.