# DOCTYPE html

## Explicación

El DOCTYPE es una declaración que indica al navegador qué versión de HTML se está utilizando. Para HTML5, se utiliza `<!DOCTYPE html>`.

Esta declaración debe ser la primera línea de cualquier documento HTML.

## Ejemplo básico

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Mi página</title>
</head>
<body>
    <h1>Hola Mundo</h1>
</body>
</html>
```

## Ejemplo de la vida real

En un sitio web de una empresa, el DOCTYPE asegura que el navegador renderice la página correctamente.

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Empresa XYZ</title>
</head>
<body>
    <header>
        <h1>Bienvenido a Empresa XYZ</h1>
    </header>
    <main>
        <p>Contenido de la página...</p>
    </main>
</body>
</html>
```

## Notas importantes

- Sin DOCTYPE, el navegador puede entrar en modo quirks, lo que puede causar problemas de renderizado.
- Es case-insensitive, pero se recomienda en mayúsculas.

## Mejores prácticas

- Siempre incluye el DOCTYPE al inicio de cada documento HTML.
- Usa `<!DOCTYPE html>` para HTML5.