# Lectores de pantalla (alt text, labels, headings)

Compatibilidad con tecnologías de asistencia.

## Imágenes

Alt text descriptivo.

**Ejemplo bueno**:

```html
<img src="grafico-ventas.png" alt="Gráfico de barras mostrando aumento de ventas del 25% en Q4">
```

**Ejemplo malo**:

```html
<img src="grafico.png" alt="Gráfico">
```

## Formularios

Labels asociados.

**Ejemplo**:

```html
<label for="busqueda">Buscar productos:</label>
<input id="busqueda" type="search" aria-describedby="ayuda-busqueda">
<div id="ayuda-busqueda">Busca por nombre o categoría</div>
```

## Estructura

Headings y landmarks.

**Ejemplo**:

```html
<h1>Tienda Online</h1>
<h2>Categorías</h2>
<section aria-labelledby="electronica">
    <h3 id="electronica">Electrónica</h3>
    <!-- productos -->
</section>
```

**Notas importantes**: Probar con lector de pantalla real. Evitar "clic aquí" en enlaces.