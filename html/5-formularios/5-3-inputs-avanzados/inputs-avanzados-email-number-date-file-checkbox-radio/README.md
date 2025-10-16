# Inputs avanzados (email, number, date, file, checkbox, radio)

## Explicación

Tipos de input especializados:

- email: Para emails.
- number: Para números.
- date: Para fechas.
- file: Para archivos.
- checkbox: Para opciones múltiples.
- radio: Para opciones únicas.

## Ejemplo básico

```html
<input type="email" name="email">
<input type="number" name="age" min="0" max="120">
<input type="date" name="birthdate">
<input type="file" name="photo">
<input type="checkbox" name="agree" value="yes"> Acepto
<input type="radio" name="gender" value="male"> Masculino
```

## Ejemplo de la vida real

En un formulario de registro.

```html
<form>
    <input type="email" name="email" placeholder="tu@email.com" required>
    <input type="date" name="birthdate">
    <input type="checkbox" name="newsletter"> Suscribirme al newsletter
    <input type="radio" name="plan" value="basic"> Básico
    <input type="radio" name="plan" value="premium"> Premium
</form>
```

## Notas importantes

- Navegadores validan automáticamente.
- file permite múltiples archivos con multiple.

## Mejores prácticas

- Usa tipos apropiados para mejor UX.
- Valida en cliente y servidor.