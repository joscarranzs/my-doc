# Patterns de diseño (Observer, Module, Singleton)

Patrones comunes para resolver problemas.

- Observer: Notificar cambios.
- Module: Encapsular código.
- Singleton: Una instancia única.

**Ejemplo de la vida real**: Singleton para configuración.

```javascript
class Config {
    constructor() {
        if (Config.instance) return Config.instance;
        this.settings = {};
        Config.instance = this;
    }
}

let config1 = new Config();
let config2 = new Config();
console.log(config1 === config2); // true
```