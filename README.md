# cool things notes


# Web sites
  * Github Diagrams <br>
    ```
    https://mermaid.live
    ``` 

  * Entity-Relationship Diagrams <br>
    ```
    https://dbdiagram.io/home
    ```

  * Online in One Line <br>
    ```
    https://ngrok.com/
    ```

  * Logos <br>
    ```
    https://looka.com/explore
    ```

  * Autocomplete code <br>
    ```
    https://www.useblackbox.io/
    ```


# ML notes

### Credenciales de Usuario

- **Username:** ext_pebidogg
- **Email:** ext_pebidogg@mercadolivre.com
- **Password:** Cl4v3d3m13rd4+12
- **PIN:** 2205870522

### Base de Datos Local

- **Local MySQL Password:** claveLocalMySQL

### Ubuntu

- **Ruta donde están los repos:** `/mnt/c/EDF`

### Tokens y Autenticación

- **X-Tiger-Token:** Bearer
- **X-Auth:** ext_pebidogg-a9b7dd51-47c5-4ea3-b253-634550c55b12
- **Mordor, console, app, cookies, session id:** ext_pebidogg-a9b7dd51-47c5-4ea3-b253-634550c55b12

### Enlaces Útiles

- Realiza Pruebas - MercadoLibre - https://developers.mercadolibre.com.ar/es_ar/realiza-pruebas
- API Sites - MercadoLibre - https://api.mercadolibre.com/sites/

### GitHub

- **Volver a ejecutar el pipeline en GitHub:** `rp retest`

### WiFi Polo Dot

- **Account Username:** ext_pedbidogg@mercadolivre.com
- **Guest Password:** kt2iqx


¡Por supuesto! Aquí tienes el texto formateado:

```markdown
## Crear una versión para una nueva release en Fury

### Pasos a seguir:

1. **Ejecutar el comando en el editor de código:**
   ```sh
   $ fury create-version 0.0.XX-test-X
   ```

   Por ejemplo:
   ```sh
   $ fury create-version 0.0.10-test-2
   ```

2. **Checkear que aparezca en Fury como un nuevo deployment:**
   Nuevo Deployment en Fury

3. **Activar en Fury si está inactivo:**
   Activar en Fury

4. **Modificar la configuración si es necesario:**
   Modificar Configuración

   Selecciona la versión que quieres activar y la configuración.

   En este caso, activa el scope:
   - **Scope:** "test"
   - **Version:** "0.0.XX-test-X"

5. **Revisar en la configuración que haga 1 test.**

6. **En caso de error, hacer un rollback:**
   Rollback en Fury

### Pipeline Configuration

- **Config Release Deployment**
- **Strategy to use:** Blue green
- **Block size:** 60
- **Swap interval:** 10
- **Max failures:** 1
- **Pool size increment:** 1


### Go tests
```sh
# Ejecuta las pruebas unitarias en el paquete especificado con detalles y cobertura de código.
go test -v -cover ./internal/modules/comment/adapters
```

Este comando realiza lo siguiente:
- `go test`: Ejecuta las pruebas unitarias en Go.
- `-v`: Muestra detalles adicionales durante la ejecución de las pruebas (modo detallado).
- `-cover`: Genera un informe de cobertura de código, indicando qué partes del código fueron ejecutadas durante las pruebas.
- `./internal/modules/comment/adapters`: Especifica el paquete donde se encuentran las pruebas a ejecutar.

### Go exports

```sh
# Añade el directorio bin de GOPATH al PATH del sistema
export PATH=$(go env GOPATH)/bin:$PATH

# Configura GOPRIVATE para excluir ciertos repositorios de la verificación de módulos
export GOPRIVATE=github.com/mercadolibre/*,github.com/melisource/*
```

### Bash
```bash
#!/bin/bash

# Este script recarga el archivo .bashrc
source ~/.bashrc

# Cambiar al directorio raíz
cd /

# Cambiar al directorio /mnt/c/EDF/
cd ./mnt/c/EDF/

# Puedes agregar más comandos aquí
echo "El archivo .bashrc ha sido recargado y se ha cambiado al directorio /mnt/c/EDF/"
```

Para mostrar la rama de Git entre paréntesis en el prompt de la consola en Visual Studio Code, puedes modificar la función y el prompt de la siguiente manera:

Abre tu archivo .bashrc (o .zshrc si usas Zsh) en tu directorio de usuario:
```
nano ~/.bashrc
```
Agrega la siguiente función para obtener la rama de Git actual:
```
parse_git_branch() {
    git branch 2>/dev/null | grep '*' | sed 's/* \(.*\)/ (\1)/'
}
```
Actualiza el prompt para incluir la rama de Git entre paréntesis. Añade esta línea al final del archivo .bashrc:
```
export PS1="\u@\h \[\033[32m\]\w\[\033[33m\]\$(parse_git_branch)\[\033[00m\] $ "
```
Guarda los cambios y recarga el archivo .bashrc con el siguiente comando:
```
source ~/.bashrc
```
