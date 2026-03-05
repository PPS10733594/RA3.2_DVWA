### 11. CSP Bypass

- **Objetivo:** Eludir las políticas de seguridad de contenido (Content Security Policy - CSP) que intentan mitigar ataques XSS.

- **Procedimiento:**
    1. **Análisis de la CSP:** Inspeccionamos las cabeceras HTTP para ver qué está permitido. En este caso, la política permite scripts desde ciertos orígenes.
    2. **Inyección del Payload:** Introducimos código que intenta eludir la política.
        ```html
        <script>alert(document.cookie)</script>
        ```

- **Resultado:**
    La aplicación ejecuta nuestro script, demostrando que la política CSP tiene una configuración débil que puede ser eludida.
    
    ## Resultado
    ![Captura del ejercicio](../assets/cspbypass.png)
