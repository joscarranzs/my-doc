# Accesibilidad básica

## Explicación

La accesibilidad asegura que el sitio sea usable por personas con discapacidades.

## Ejemplo básico

```html
<img src="foto.jpg" alt="Descripción detallada">
<a href="#main">Saltar al contenido</a>
```

## Ejemplo de la vida real

En un formulario accesible.

```html
<label for="email">Email:</label>
<input id="email" type="email" aria-describedby="email-help">
<span id="email-help">Ingresa tu email válido</span>
```

## Notas importantes

- Usa alt en imágenes.
- Etiquetas en formularios.

## Mejores prácticas

- Prueba con lectores de pantalla.
- Sigue las guías WCAG.