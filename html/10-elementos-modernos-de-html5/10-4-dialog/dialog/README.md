# Dialog

## Explicación

Elemento para modales y diálogos.

## Ejemplo básico

```html
<dialog id="myDialog">
    <p>¿Estás seguro?</p>
    <button onclick="dialog.close()">Cancelar</button>
    <button onclick="confirmAction()">Confirmar</button>
</dialog>
<script>
    const dialog = document.getElementById('myDialog');
    dialog.showModal();
</script>
```

## Ejemplo de la vida real

En un formulario de confirmación.

```html
<dialog>
    <form method="dialog">
        <p>Eliminar este elemento?</p>
        <button value="cancel">Cancelar</button>
        <button value="confirm">Eliminar</button>
    </form>
</dialog>
```

## Notas importantes

- showModal() para modal.
- method="dialog" en forms.

## Mejores prácticas

- Maneja foco y teclado.
- Backdrop automático.