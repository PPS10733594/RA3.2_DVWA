### 1. Brute Force

- **Objetivo:** Demostrar la vulnerabilidad de un formulario de login ante un ataque de fuerza bruta, probando múltiples combinaciones de contraseña hasta encontrar la correcta.

- **Procedimiento:**
    1. **Análisis Inicial:** Identificamos que el formulario de login no tiene un mecanismo de bloqueo por múltiples intentos fallidos, lo que lo hace susceptible a un ataque de diccionario.
    2. **Creación del Script:** Para un ataque más dirigido, creamos un script en Python que automatiza las peticiones al formulario de login.
    3. **Ataque con Hydra:** También utilizamos `hydra` desde la terminal para automatizar el ataque. Especificamos el usuario (`-l admin`), el archivo con el diccionario de contraseñas (`-P /home/kali/rockyou.txt`) y la URL objetivo.
        ```bash
        hydra -l admin -P /home/kali/rockyou.txt 'http-get://localhost:8080/vulnerabilities/brute/'
        ```

- **Resultado:**
    Hydra probó exitosamente miles de contraseñas y encontró varias válidas para el usuario "admin", siendo `password` una de ellas.
    
    ![Resultado del ataque de fuerza bruta con Hydra](./Captura%20de%20pantalla%202026-03-04%20171951.png)
