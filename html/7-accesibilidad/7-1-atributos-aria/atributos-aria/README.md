# Atributos ARIA

## Explicación

ARIA (Accessible Rich Internet Applications) añade información de accesibilidad.

## Ejemplo básico

```html
<button aria-label="Cerrar menú">×</button>
<div role="alert" aria-live="assertive">Error: Campo requerido</div>
```

## Ejemplo de la vida real

En un acordeón.

```html
<button aria-expanded="false" aria-controls="panel1">Sección 1</button>
<div id="panel1" aria-labelledby="heading1" hidden>
    Contenido...
</div>
```

## Notas importantes

- Usa cuando HTML nativo no basta.
- No reemplaza buena semántica.

## Mejores prácticas

- Prueba con lectores de pantalla.
- Actualiza dinámicamente.