# Atributos importantes (href, src, alt, target)

## Explicación

- href: URL del enlace.
- src: Fuente de la imagen/recurso.
- alt: Texto alternativo para imágenes.
- target: Cómo abrir el enlace (_blank, _self, etc.).

## Ejemplo básico

```html
<a href="pagina.html" target="_blank">Enlace</a>
<img src="logo.png" alt="Logo de la empresa">
```

## Ejemplo de la vida real

En un enlace externo.

```html
<a href="https://externo.com" target="_blank" rel="noopener">Visitar sitio externo</a>
```

## Notas importantes

- target="_blank" abre en nueva pestaña.
- alt describe la imagen para lectores de pantalla.

## Mejores prácticas

- Usa rel="noopener" con target="_blank" por seguridad.
- Alt descriptivo y conciso.