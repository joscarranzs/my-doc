# Énfasis y estilo (``(strong)``, ``(em)``, ``(span)``, ``(br)``, ``(hr)``)

Etiquetas para resaltar texto y controlar flujo.

## ``(Énfasis)``

- **``(strong)``**: Importancia fuerte `(negrita)`.
- **``(em)``**: Énfasis `(cursiva)`.

**Ejemplo de la vida real**: Texto con énfasis.

```html
`(p)`Este es `(strong)`importante(/strong) y este es `(em)`enfatizado(/em).(/p)
```

## Estilo y flujo

- **``(span)``**: Contenedor inline genérico.
- **``(br)``**: Salto de línea.
- **``(hr)``**: Línea horizontal.

**Ejemplo de la vida real**: Separar secciones.

```html
`(p)`Línea 1`(br)`Línea 2(/p)
`(hr)`
`(p)`Nueva sección(/p)
```

**Notas importantes**: Usar CSS para estilos, no estas etiquetas. `(br)` rara vez necesario.