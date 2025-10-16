# Destructuring avanzado

Extraer valores anidados o con valores por defecto.

**Ejemplo de la vida real**: Configurando opciones de función.

```javascript
function configurar({ tema = "claro", idioma = "es" } = {}) {
    console.log(`Tema: ${tema}, Idioma: ${idioma}`);
}

configurar({ tema: "oscuro" }); // Tema: oscuro, Idioma: es
```