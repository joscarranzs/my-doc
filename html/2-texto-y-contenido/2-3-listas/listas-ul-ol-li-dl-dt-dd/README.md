# Listas (ul, ol, li, dl, dt, dd)

## Explicación

- ul: Lista no ordenada.
- ol: Lista ordenada.
- li: Elemento de lista.
- dl: Lista de definiciones.
- dt: Término.
- dd: Definición.

## Ejemplo básico

```html
<ul>
    <li>Elemento 1</li>
    <li>Elemento 2</li>
</ul>

<ol>
    <li>Primero</li>
    <li>Segundo</li>
</ol>

<dl>
    <dt>HTML</dt>
    <dd>Lenguaje de marcado</dd>
</dl>
```

## Ejemplo de la vida real

En un menú de navegación.

```html
<nav>
    <ul>
        <li><a href="/">Inicio</a></li>
        <li><a href="/about">Acerca</a></li>
    </ul>
</nav>
```

## Notas importantes

- li solo dentro de ul/ol.
- dl para pares término-definición.

## Mejores prácticas

- Usa listas para contenido estructurado.
- Evita listas para diseño, usa CSS.