# Roles y navegación con lectores de pantalla

## Explicación

Roles ARIA definen el propósito de elementos. Navegación accesible.

## Ejemplo básico

```html
<nav role="navigation">
    <ul>
        <li><a href="/">Inicio</a></li>
    </ul>
</nav>
```

## Ejemplo de la vida real

En un formulario.

```html
<form role="search">
    <label for="search">Buscar:</label>
    <input id="search" type="search">
    <button type="submit">Buscar</button>
</form>
```

## Notas importantes

- Roles implícitos en etiquetas semánticas.
- Usa landmarks para navegación.

## Mejores prácticas

- Prueba navegación por teclado.
- Evita roles redundantes.