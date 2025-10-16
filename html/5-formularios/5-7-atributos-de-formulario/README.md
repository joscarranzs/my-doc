# Atributos de formulario (action, method, enctype)

Controlan envío y procesamiento.

## action

URL donde enviar datos.

**Ejemplo**:

```html
(form action="/procesar-formulario" method="post")
```

## method

GET (datos en URL) o POST (datos en body).

**Ejemplo de la vida real**: Búsqueda vs envío de datos.

```html
(form action="/buscar" method="get") (!-- Datos visibles en URL --)
(form action="/contacto" method="post") (!-- Datos ocultos --)
```

## enctype

Codificación para envío de archivos.

**Ejemplo**:

```html
(form action="/upload" method="post" enctype="multipart/form-data")
    (input type="file" name="archivo")
(/form)
```

**Notas importantes**: GET limitado a ~2048 caracteres. POST para datos sensibles o grandes.