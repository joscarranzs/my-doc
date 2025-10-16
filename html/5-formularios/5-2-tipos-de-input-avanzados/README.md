# Tipos de input avanzados ((input type="date"), (input type="file"), etc.)

Inputs especializados para datos específicos.

## Fecha y hora

- **date**: Selector de fecha.
- **time**: Selector de hora.
- **datetime-local**: Fecha y hora local.

**Ejemplo de la vida real**: Reserva de cita.

```html
(label for="fecha")Fecha de cita:(/label)
(input type="date" id="fecha" name="fecha" required)
```

## Archivos

**file**: Subida de archivos.

**Ejemplo de la vida real**: Subir CV.

```html
(input type="file" name="cv" accept=".pdf,.doc" multiple)
```

## Otros tipos

- **range**: Slider numérico.
- **color**: Selector de color.
- **search**: Campo de búsqueda.

**Ejemplo de la vida real**: Configuración de perfil.

```html
(label)Volumen: (input type="range" min="0" max="100" value="50")(/label)
(input type="color" name="color_favorito")
```

**Notas importantes**: Soporte varía por navegador. Usar polyfills si necesario.