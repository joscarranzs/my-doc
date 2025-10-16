# Lista de tareas avanzada

To-do list con categorías y prioridades.

## HTML

```html
<div class="app-tareas">
    <h1>Lista de Tareas</h1>
    
    <form id="form-tarea">
        <input type="text" id="titulo-tarea" placeholder="Título de la tarea" required>
        <textarea id="descripcion-tarea" placeholder="Descripción"></textarea>
        <select id="prioridad-tarea">
            <option value="baja">Baja</option>
            <option value="media">Media</option>
            <option value="alta">Alta</option>
        </select>
        <select id="categoria-tarea">
            <option value="trabajo">Trabajo</option>
            <option value="personal">Personal</option>
            <option value="estudio">Estudio</option>
        </select>
        <input type="date" id="fecha-limite">
        <button type="submit">Agregar Tarea</button>
    </form>
    
    <div class="filtros">
        <button class="filtro activo" data-filtro="todas">Todas</button>
        <button class="filtro" data-filtro="pendientes">Pendientes</button>
        <button class="filtro" data-filtro="completadas">Completadas</button>
    </div>
    
    <div id="lista-tareas"></div>
</div>
```

## JavaScript

```javascript
let tareas = JSON.parse(localStorage.getItem('tareas')) || [];

function mostrarTareas(filtro = 'todas') {
    const lista = document.getElementById('lista-tareas');
    lista.innerHTML = '';
    
    let tareasFiltradas = tareas;
    
    if (filtro === 'pendientes') {
        tareasFiltradas = tareas.filter(t => !t.completada);
    } else if (filtro === 'completadas') {
        tareasFiltradas = tareas.filter(t => t.completada);
    }
    
    tareasFiltradas.forEach((tarea, index) => {
        const divTarea = document.createElement('div');
        divTarea.className = `tarea ${tarea.prioridad} ${tarea.completada ? 'completada' : ''}`;
        divTarea.innerHTML = `
            <div class="contenido-tarea">
                <h3>${tarea.titulo}</h3>
                <p>${tarea.descripcion || ''}</p>
                <div class="meta">
                    <span class="categoria">${tarea.categoria}</span>
                    <span class="fecha">${tarea.fechaLimite ? new Date(tarea.fechaLimite).toLocaleDateString() : ''}</span>
                </div>
            </div>
            <div class="acciones">
                <button onclick="toggleCompletada(${index})">${tarea.completada ? 'Desmarcar' : 'Completar'}</button>
                <button onclick="editarTarea(${index})">Editar</button>
                <button onclick="eliminarTarea(${index})">Eliminar</button>
            </div>
        `;
        lista.appendChild(divTarea);
    });
}

document.getElementById('form-tarea').addEventListener('submit', function(e) {
    e.preventDefault();
    const nuevaTarea = {
        titulo: document.getElementById('titulo-tarea').value,
        descripcion: document.getElementById('descripcion-tarea').value,
        prioridad: document.getElementById('prioridad-tarea').value,
        categoria: document.getElementById('categoria-tarea').value,
        fechaLimite: document.getElementById('fecha-limite').value,
        completada: false,
        fechaCreacion: new Date().toISOString()
    };
    
    tareas.push(nuevaTarea);
    guardarTareas();
    mostrarTareas();
    this.reset();
});

function toggleCompletada(index) {
    tareas[index].completada = !tareas[index].completada;
    guardarTareas();
    mostrarTareas();
}

function eliminarTarea(index) {
    tareas.splice(index, 1);
    guardarTareas();
    mostrarTareas();
}

function editarTarea(index) {
    // Implementar edición
    alert('Función de edición no implementada aún');
}

function guardarTareas() {
    localStorage.setItem('tareas', JSON.stringify(tareas));
}

// Filtros
document.querySelectorAll('.filtro').forEach(boton => {
    boton.addEventListener('click', function() {
        document.querySelectorAll('.filtro').forEach(b => b.classList.remove('activo'));
        this.classList.add('activo');
        mostrarTareas(this.dataset.filtro);
    });
});

mostrarTareas();
```

**Objetivo**: Practicar CRUD avanzado, filtros, localStorage.