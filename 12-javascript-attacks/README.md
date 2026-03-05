### 12. JavaScript Attacks

- **Objetivo:** Comprender que la lógica de validación implementada del lado del cliente (JavaScript) puede ser manipulada o eludida fácilmente por un atacante.

- **Procedimiento:**
    1. **Análisis del Código:** Inspeccionamos el código fuente de la página. Vemos que hay una función JavaScript que valida que la palabra "success" sea introducida. Esta validación ocurre solo en el navegador.
    2. **Bypass de la Validación:** Abrimos la consola de desarrollador del navegador (F12). Buscamos la función que realiza la comprobación y ejecutamos la función que da por válido el resultado.
        ```javascript
        // Ejecutamos esto en la consola del navegador
        win();
        ```

- **Resultado:**
    Al ejecutar el comando en la consola, forzamos la finalización del "juego" y obtenemos el mensaje "Well done!", demostrando que la seguridad del lado del cliente no es suficiente.
    
    ## Resultado
    ![Captura del ejercicio](../assets/javascriptattacks.png)
