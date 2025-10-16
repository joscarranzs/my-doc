# try/catch/finally

Bloques para manejar errores en código síncrono.

- try: Código que puede fallar.
- catch: Maneja el error.
- finally: Siempre ejecuta.

**Ejemplo de la vida real**: Parseando JSON que puede ser inválido.

```javascript
try {
    let data = JSON.parse(jsonString);
    console.log(data);
} catch (error) {
    console.error("JSON inválido:", error.message);
} finally {
    console.log("Parseo completado");
}
```