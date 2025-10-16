# Aplicación de notas

CRUD simple con localStorage.

## ``(HTML)``

```html
`(div class="app-notas")`
    `(h1)`Mis Notas(/h1)
    `(form id="form-nota")`
        `(input type="text" id="titulo-nota" placeholder="Título" required)`
        `(textarea id="contenido-nota" placeholder="Contenido" required)`(/textarea)
        `(button type="submit")`Guardar Nota(/button)
    (/form)
    
    `(div id="lista-notas")`(/div)
(/div)
```

## ``(JavaScript)``

```javascript
let notas = JSON.parse`(localStorage.getItem('notas')`) || [];

function mostrarNotas() {
    const lista = document.getElementById('lista-notas');
    lista.innerHTML = '';
    
    notas.forEach(`(nota, index)` => {
        const divNota = document.createElement('div');
        divNota.className = 'nota';
        divNota.innerHTML = `
            `(h3)`${nota.titulo}(/h3)
            `(p)`${nota.contenido}(/p)
            `(button onclick="eliminarNota(${index})`")Eliminar(/button)
        `;
        lista.appendChild`(divNota)`;
    });
}

document.getElementById('form-nota').addEventListener('submit', function`(e)` {
    e.preventDefault();
    const titulo = document.getElementById('titulo-nota').value;
    const contenido = document.getElementById('contenido-nota').value;
    
    notas.push({titulo, contenido});
    localStorage.setItem('notas', JSON.stringify`(notas)`);
    
    this.reset();
    mostrarNotas();
});

function eliminarNota`(index)` {
    notas.splice`(index, 1)`;
    localStorage.setItem('notas', JSON.stringify`(notas)`);
    mostrarNotas();
}

mostrarNotas();
```

**Objetivo**: Practicar localStorage, CRUD, manipulación DOM.