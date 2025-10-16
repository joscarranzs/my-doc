# Galería de imágenes

Mostrar imágenes en grid responsivo.

## HTML básico

```html
`(section class="galeria")`
    `(h2)`Mis Fotos(/h2)
    `(div class="grid-imagenes")`
        `(figure)`
            `(img src="foto1.jpg" alt="Descripción foto 1" loading="lazy")`
            `(figcaption)`Descripción de la foto 1(/figcaption)
        (/figure)
        `(figure)`
            `(img src="foto2.jpg" alt="Descripción foto 2" loading="lazy")`
            `(figcaption)`Descripción de la foto 2(/figcaption)
        (/figure)
        (!-- Más imágenes --)
    (/div)
(/section)
```

## Modal para vista ampliada

```html
`(div id="modal" class="modal")`
    `(span class="cerrar")`&times;(/span)
    `(img id="imagen-modal" class="imagen-modal")`
    `(div id="caption")`(/div)
(/div)
```

## JavaScript para modal

```javascript
const modal = document.getElementById('modal');
const imagenes = document.querySelectorAll('.grid-imagenes img');

imagenes.forEach(img => {
    img.onclick = function() {
        modal.style.display = 'block';
        document.getElementById('imagen-modal').src = this.src;
        document.getElementById('caption').innerHTML = this.alt;
    }
});
```

**Objetivo**: Practicar multimedia, CSS Grid, JavaScript básico.