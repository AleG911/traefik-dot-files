# Traefik v2

Este repositorio consisten en una serie de archivos para facilitar el deployment de traefik en pocos minutos. Este contempla configuración dinámica y estática. Además de algunos middlewares básicos deseables.

---

1. Instalar las dependencias para docker: ***(método alternativo, se recomienda)***
    ```bash
    sudo apt update
    sudo apt install docker docker-compose
    ```


2. Generar el hash del usuario y contraseña para proteger el panel de Traefik.

    ```bash
    sudo apt update
    sudo apt install apache2-utils
    ```

    Generar el usuario:
    ```bash
    echo $(htpasswd -nb <USUARIO> <CONTRASEÑA>) | sed -e s/\\$/\\$\\$/g
    ```

3. Clonar este repositorio.

    ```bash
    git clone https://github.com/AleG911/traefik-dot-files.git
    ```
4. Modificar el archivo **.env** con el email asociado a la cuenta de Cloudflare, el API Key y el usuario generado previamente.
