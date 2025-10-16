# Seguridad básica `(XSS, CSRF prevention)`

Proteger contra ataques comunes.

## XSS `(Cross-Site Scripting)`

Prevenir inyección de scripts.

**Ejemplo vulnerable**:

```html
`(div)`Comentario: (?php echo $_POST['comentario']; ?)(/div)
```

**Ejemplo seguro**:

```html
`(div)`Comentario: (?php echo htmlspecialchars($_POST['comentario']); ?)(/div)
```

## Content Security Policy `(CSP)`

Política de seguridad de contenido.

**Ejemplo**:

```html
`(meta http-equiv="Content-Security-Policy" content="default-src 'self'; script-src 'self' https://apis.google.com")`
```

## CSRF Protection

Tokens para prevenir cross-site request forgery.

**Ejemplo**:

```html
`(form action="/transferir" method="post")`
    `(input type="hidden" name="csrf_token" value="token-generado")`
    `(input type="number" name="monto")`
    `(button type="submit")`Transferir(/button)
(/form)
```

**Notas importantes**: Validar y sanitizar todas las entradas. Usar HTTPS. Mantener software actualizado.