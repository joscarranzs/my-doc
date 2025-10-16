# Editor de texto simple

Editor básico con formato y guardado.

## HTML

```html
<div class="editor-texto">
    <h1>Editor de Texto</h1>
    
    <div class="barra-herramientas">
        <button id="negrita" title="Negrita"><strong>B</strong></button>
        <button id="italica" title="Itálica"><em>I</em></button>
        <button id="subrayado" title="Subrayado"><u>U</u></button>
        <select id="tamano-fuente">
            <option value="12px">12px</option>
            <option value="14px">14px</option>
            <option value="16px">16px</option>
            <option value="18px">18px</option>
            <option value="24px">24px</option>
        </select>
        <input type="color" id="color-texto" title="Color del texto">
        <button id="guardar">💾 Guardar</button>
        <button id="cargar">📁 Cargar</button>
        <button id="nuevo">🆕 Nuevo</button>
    </div>
    
    <div class="editor" id="editor" contenteditable="true">
        <p>Empieza a escribir aquí...</p>
    </div>
    
    <div class="estadisticas">
        <span id="contador-palabras">Palabras: 0</span>
        <span id="contador-caracteres">Caracteres: 0</span>
    </div>
</div>
```

## JavaScript

```javascript
const editor = document.getElementById('editor');

function ejecutarComando(comando, valor = null) {
    document.execCommand(comando, false, valor);
    editor.focus();
}

document.getElementById('negrita').addEventListener('click', () => ejecutarComando('bold'));
document.getElementById('italica').addEventListener('click', () => ejecutarComando('italic'));
document.getElementById('subrayado').addEventListener('click', () => ejecutarComando('underline'));

document.getElementById('tamano-fuente').addEventListener('change', function() {
    ejecutarComando('fontSize', this.selectedIndex + 1);
});

document.getElementById('color-texto').addEventListener('change', function() {
    ejecutarComando('foreColor', this.value);
});

function actualizarEstadisticas() {
    const texto = editor.textContent || '';
    const palabras = texto.trim() === '' ? 0 : texto.trim().split(/\s+/).length;
    const caracteres = texto.length;
    
    document.getElementById('contador-palabras').textContent = `Palabras: ${palabras}`;
    document.getElementById('contador-caracteres').textContent = `Caracteres: ${caracteres}`;
}

editor.addEventListener('input', actualizarEstadisticas);

document.getElementById('guardar').addEventListener('click', () => {
    const contenido = editor.innerHTML;
    const nombreArchivo = prompt('Nombre del archivo:', 'documento.html');
    
    if (nombreArchivo) {
        const blob = new Blob([contenido], { type: 'text/html' });
        const url = URL.createObjectURL(blob);
        
        const a = document.createElement('a');
        a.href = url;
        a.download = nombreArchivo;
        a.click();
        
        URL.revokeObjectURL(url);
    }
});

document.getElementById('cargar').addEventListener('click', () => {
    const input = document.createElement('input');
    input.type = 'file';
    input.accept = '.html,.txt';
    
    input.onchange = function(e) {
        const archivo = e.target.files[0];
        if (archivo) {
            const reader = new FileReader();
            reader.onload = function(e) {
                editor.innerHTML = e.target.result;
                actualizarEstadisticas();
            };
            reader.readAsText(archivo);
        }
    };
    
    input.click();
});

document.getElementById('nuevo').addEventListener('click', () => {
    if (confirm('¿Estás seguro de que quieres crear un nuevo documento? Se perderán los cambios no guardados.')) {
        editor.innerHTML = '<p>Empieza a escribir aquí...</p>';
        actualizarEstadisticas();
    }
});

// Atajos de teclado
document.addEventListener('keydown', function(e) {
    if (e.ctrlKey || e.metaKey) {
        switch(e.key) {
            case 'b':
                e.preventDefault();
                ejecutarComando('bold');
                break;
            case 'i':
                e.preventDefault();
                ejecutarComando('italic');
                break;
            case 'u':
                e.preventDefault();
                ejecutarComando('underline');
                break;
            case 's':
                e.preventDefault();
                document.getElementById('guardar').click();
                break;
        }
    }
});

actualizarEstadisticas();
```

**Objetivo**: Practicar execCommand API, manipulación DOM, archivos.