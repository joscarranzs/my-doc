# Enlaces (`(a)`)

Los enlaces conectan páginas y recursos.

**Sintaxis básica**:

```html
(a href="url")Texto del enlace(/a)
```

**Ejemplo de la vida real**: Menú de navegación.

```html
(nav)
    (a href="/")Inicio(/a)
    (a href="/productos")Productos(/a)
    (a href="/contacto")Contacto(/a)
(/nav)
```

**Atributos importantes**:
- **href**: URL destino.
- **target**: _blank para nueva pestaña.
- **rel**: noopener para seguridad.

**Notas importantes**: Enlaces rotos afectan UX. Usar texto descriptivo para accesibilidad.