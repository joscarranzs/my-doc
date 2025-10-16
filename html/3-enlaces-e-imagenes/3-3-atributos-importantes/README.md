# Atributos importantes `(href, src, alt, target)`

Atributos clave para enlaces e imágenes.

## ``(href)``

URL del enlace. Puede ser relativa o absoluta.

**Ejemplo**:

```html
`(a href="/contacto")`Contacto(/a)
`(a href="https://ejemplo.com")`Externo(/a)
```

## ``(src)``

Ruta de la imagen o recurso.

**Ejemplo**:

```html
`(img src="images/logo.png" alt="Logo")`
```

## ``(alt)``

Texto descriptivo para imágenes, crucial para accesibilidad.

**Ejemplo**:

```html
`(img src="perro.jpg" alt="Un perro golden retriever jugando en el parque")`
```

## ``(target)``

Controla cómo se abre el enlace.

**Ejemplo**:

```html
`(a href="https://externo.com" target="_blank" rel="noopener")`Abrir en nueva pestaña(/a)
```

**Notas importantes**: target="_blank" requiere rel="noopener" por seguridad.