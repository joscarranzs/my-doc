# Página personal básica

Proyecto simple para practicar fundamentos de HTML.

## Estructura básica

```html
(!DOCTYPE html)
(html lang="es")
(head)
    (meta charset="UTF-8")
    (meta name="viewport" content="width=device-width, initial-scale=1.0")
    (title)Mi Página Personal(/title)
(/head)
(body)
    (header)
        (h1)Juan Pérez(/h1)
        (p)Desarrollador Web(/p)
    (/header)
    
    (nav)
        (ul)
            (li)(a href="#sobre-mi")Sobre mí(/a)(/li)
            (li)(a href="#proyectos")Proyectos(/a)(/li)
            (li)(a href="#contacto")Contacto(/a)(/li)
        (/ul)
    (/nav)
    
    (main)
        (section id="sobre-mi")
            (h2)Sobre mí(/h2)
            (p)Soy un desarrollador apasionado por la tecnología...(/p)
        (/section)
        
        (section id="proyectos")
            (h2)Proyectos(/h2)
            (article)
                (h3)Proyecto 1(/h3)
                (p)Descripción del proyecto...(/p)
            (/article)
        (/section)
    (/main)
    
    (footer)
        (p)&copy; 2023 Juan Pérez(/p)
    (/footer)
(/body)
(/html)
```

## Mejoras sugeridas

- Añadir CSS para estilos.
- Incluir imagen de perfil.
- Agregar enlaces a redes sociales.

**Objetivo**: Practicar estructura semántica y navegación básica.