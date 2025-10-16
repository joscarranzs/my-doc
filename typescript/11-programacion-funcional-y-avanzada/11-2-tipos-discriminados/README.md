# Tipos discriminados

Uniones con propiedad discriminante.

**Ejemplo de la vida real**: Eventos de UI.

```typescript
interface ClickEvent {
    type: "click";
    x: number;
    y: number;
}

interface KeyEvent {
    type: "key";
    key: string;
}

type Evento = ClickEvent | KeyEvent;

function manejarEvento(evento: Evento) {
    if (evento.type === "click") {
        console.log(`Click en ${evento.x}, ${evento.y}`);
    } else {
        console.log(`Tecla: ${evento.key}`);
    }
}
```

**Notas importantes**: Type narrowing automático.