# Buenas prácticas de accesibilidad

## Explicación

Principios para hacer sitios accesibles.

## Ejemplo básico

```html
<img src="chart.png" alt="Gráfico de ventas: enero 100k, febrero 120k">
<a href="#main">Saltar al contenido principal</a>
```

## Ejemplo de la vida real

En un sitio corporativo.

```html
<body>
    <a href="#main-content" class="sr-only">Saltar navegación</a>
    <header>...</header>
    <main id="main-content">
        <h1>Contenido principal</h1>
        ...
    </main>
</body>
```

## Notas importantes

- Contraste de color adecuado.
- Tamaño de fuente legible.

## Mejores prácticas

- Sigue WCAG 2.1.
- Incluye personas con discapacidades en testing.