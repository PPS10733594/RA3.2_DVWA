### 7. SQL Injection (Blind)

- **Objetivo:** Extraer información de la base de datos cuando la aplicación no muestra errores ni resultados de consultas, pero su comportamiento (respuesta Sí/No) varía según el resultado de la consulta.

- **Procedimiento:**
    1. **Creación del Script (Python):** Creamos un script en Python que automatiza las consultas booleanas para adivinar la información carácter por carácter, basándose en si la respuesta contiene "User ID exists" o no.
    2. **Extracción de Datos:** Ejecutamos el script para obtener datos como la longitud y versión de la base de datos.
        ```bash
        python3 injection.py
        ```

- **Resultado:**
    El script interactúa con la aplicación y, basándose en las respuestas, logra extraer información como la longitud y, eventualmente, el nombre de la base de datos o su versión.
    
    ## Resultado
    ![Captura del ejercicio](../assets/sqlblind.png)
