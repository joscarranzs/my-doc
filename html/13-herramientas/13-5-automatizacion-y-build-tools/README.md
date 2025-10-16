# Automatización y build tools

Optimizar workflow de desarrollo.

## Task runners

### npm scripts
```json
{
  "scripts": {
    "dev": "live-server",
    "build": "html-minifier --input-dir src --output-dir dist",
    "test": "html-validate src/**/*.html"
  }
}
```

### Gulp
```javascript
const gulp = require('gulp');
const htmlmin = require('gulp-htmlmin');

gulp.task('minify', () => {
  return gulp.src('src/*.html')
    .pipe(htmlmin({ collapseWhitespace: true }))
    .pipe(gulp.dest('dist'));
});
```

## Build tools modernos

### Vite
- **Configuración**: Cero configuración
- **Hot reload**: Instantáneo
- **Build**: Optimizado

### Parcel
- **Automágico**: Sin configuración
- **Rápido**: Build paralelo
- **Soporte**: Múltiples formatos

## Preprocesadores

### Pug (HTML)
```pug
doctype html
html(lang="es")
  head
    title Mi Página
  body
    h1= titulo
    p= descripcion
```

### Sass/SCSS (CSS)
```scss
$primary-color: #007bff;

.button {
  background: $primary-color;
  
  &:hover {
    background: darken($primary-color, 10%);
  }
}
```

## Optimización

### Herramientas
- **HTMLMinifier**: Minificar HTML
- **Imagemin**: Optimizar imágenes
- **Critical CSS**: CSS crítico inline

**Consejo**: Automatiza tareas repetitivas. Enfócate en código, no en configuración.