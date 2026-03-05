### 4. File Inclusion

- **Objetivo:** Explotar un parámetro de archivo para incluir y visualizar archivos sensibles del servidor (Path Traversal / Local File Inclusion).

- **Procedimiento:**
    1. **Identificar el Vector:** La aplicación incluye páginas mediante un parámetro `page` en la URL (ej. `?page=include.php`).
    2. **Path Traversal:** Modificamos el parámetro para intentar salir del directorio de la aplicación web y acceder a archivos del sistema. El objetivo es el archivo de contraseñas de Linux.
        ```
        http://localhost:8080/vulnerabilities/fi/?page=/etc/passwd
        ```

- **Resultado:**
    La aplicación web devuelve el contenido del archivo `/etc/passwd`, listando todos los usuarios del sistema operativo. Esta información es crucial para un atacante.
    
    ## Resultado
    ![Captura del ejercicio](../assets/fileinclusion.png)
