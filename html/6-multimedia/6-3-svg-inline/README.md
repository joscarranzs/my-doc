# SVG inline (<svg>)

Gráficos vectoriales escalables en HTML.

**Ejemplo básico**:

```html
<svg width="100" height="100">
    <circle cx="50" cy="50" r="40" fill="blue" />
</svg>
```

**Ejemplo de la vida real**: Icono interactivo.

```html
<svg width="24" height="24" viewBox="0 0 24 24">
    <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z" fill="gold"/>
</svg>
```

**Ventajas**:
- Escalables sin pérdida de calidad.
- Pequeño tamaño de archivo.
- Manipulables con CSS/JS.

**Notas importantes**: Usar viewBox para responsividad. Accesibles con aria atributos.