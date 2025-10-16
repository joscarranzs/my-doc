# Data attributes (data-*)

## Explicación

Atributos personalizados para almacenar datos.

## Ejemplo básico

```html
<div data-id="123" data-category="product">Producto</div>
```

## Ejemplo de la vida real

En una lista de productos.

```html
<ul>
    <li data-product-id="1" data-price="29.99">Libro A</li>
    <li data-product-id="2" data-price="19.99">Libro B</li>
</ul>
<script>
    // JavaScript puede acceder con dataset
    const items = document.querySelectorAll('li');
    items.forEach(item => {
        console.log(item.dataset.productId, item.dataset.price);
    });
</script>
```

## Notas importantes

- Accesibles via JavaScript con dataset.
- No afectan presentación.

## Mejores prácticas

- Usa para datos específicos de app.
- Prefiere data- sobre atributos inventados.