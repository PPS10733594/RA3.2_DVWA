### 9. Cross Site Scripting (XSS) - Stored

- **Objetivo:** Inyectar código JavaScript malicioso que se almacena permanentemente en el servidor (por ejemplo, en una base de datos) y se ejecuta cada vez que un usuario visita la página afectada.

- **Procedimiento:**
    1. **Identificar el Vector:** Localizamos una funcionalidad que permita guardar datos, como un libro de visitas o un campo de comentarios.
    2. **Inyección del Payload:** Escribimos nuestro script malicioso en el campo de "Message" y un nombre cualquiera en el campo "Name".
        ```html
        <script>alert('XSS Almacenado')</script>
        ```

- **Resultado:**
    Al hacer clic en "Sign Guestbook", el mensaje se guarda. A partir de ese momento, cualquier usuario que visite la página del libro de visitas verá ejecutarse la alerta.
    
    ## Resultado
    ![Captura del ejercicio](../assets/xssstored.png)
