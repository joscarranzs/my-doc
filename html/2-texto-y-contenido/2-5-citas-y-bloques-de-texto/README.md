# Citas y bloques de texto (`(blockquote)`, `(cite)`, `(pre)`, `(code)`)

Para citar contenido y mostrar código.

## Citas

- **`(blockquote)`**: Cita en bloque.
- **`(cite)`**: Fuente de la cita.

**Ejemplo de la vida real**: Artículo citando fuente.

```html
(blockquote)
    "La web es para todos."
    (cite)Tim Berners-Lee(/cite)
(/blockquote)
```

## Código

- **`(pre)`**: Texto preformateado.
- **`(code)`**: Código inline.

**Ejemplo de la vida real**: Documentación técnica.

```html
(pre)(code)
function hola() {
    console.log("Hola mundo");
}
(/code)(/pre)
```

**Notas importantes**: (pre) preserva espacios y saltos. Usar con (code) para sintaxis.