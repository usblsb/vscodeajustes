# Visual Studio Code VSCODE

# Configuración de la carpeta SHARED en macOS para almacenar los proyectos de VsCode desde Github Proyect Manager

Esta guía proporciona instrucciones paso a paso para configurar la carpeta SHARED en macOS con los permisos adecuados.

## Objetivo

Configurar la carpeta SHARED para que:

- Sea accesible por el sistema operativo y sus aplicaciones
- Sea accesible por usuarios admin y usuarios de la máquina
- No sea accesible públicamente desde fuera del ordenador
- Pueda ser utilizada por entornos como Python y Node.js

## Pasos

1. Abrir Terminal
2. Navegar a la carpeta de usuarios:
    
    ```
    cd /Users
    
    ```
    
3. Restablecer permisos a cero (solo root tendrá acceso):
    
    ```
    sudo chmod 000 Shared
    
    ```
    
4. Cambiar el propietario a root y el grupo a admin:
    
    ```
    sudo chown root:admin Shared
    
    ```
    
5. Establecer permisos básicos (lectura y ejecución para todos, escritura solo para root):
    
    ```
    sudo chmod 755 Shared
    
    ```
    
6. Añadir ACL para el grupo admin:
    
    ```
    sudo chmod +a "group:admin allow list,add_file,search,add_subdirectory,delete_child,readattr,writeattr,readextattr,writeextattr,readsecurity,file_inherit,directory_inherit" Shared
    
    ```
    
7. Añadir ACL para el grupo staff (usuarios estándar del Mac):
    
    ```
    sudo chmod +a "group:staff allow list,add_file,search,add_subdirectory,delete_child,readattr,writeattr,readextattr,writeextattr,readsecurity,file_inherit,directory_inherit" Shared
    
    ```
    
8. Verificar los permisos:
    
    ```
    ls -le Shared
    
    ```
    
9. Si es necesario, ajustar permisos para aplicaciones específicas:
    
    ```
    sudo chmod +a "group:_developer allow list,add_file,search,add_subdirectory,delete_child,readattr,writeattr,readextattr,writeextattr,readsecurity,file_inherit,directory_inherit" Shared
    
    ```
    
10. Reiniciar el Finder para aplicar cambios en la interfaz gráfica:
    
    ```
    killall Finder
    
    ```
    

## Verificación

1. Intenta crear un archivo en la carpeta Shared desde Terminal:
    
    ```
    touch /Users/Shared/test.txt
    
    ```
    
2. Verifica que puedes acceder a la carpeta desde Finder:
    - Abre Finder
    - Presiona Cmd+Shift+G
    - Escribe "/Users/Shared" y pulsa Enter
3. Prueba ejecutar un script de Python o Node.js que acceda a archivos en esta carpeta.

## Notas adicionales

- Esta configuración permite el acceso a la carpeta Shared desde la máquina local, pero no la hace accesible desde fuera del ordenador.
- Para uso con Python o Node.js, asegúrate de que los scripts se ejecuten con los permisos adecuados (usuario o grupo con acceso).
- Si necesitas acceso remoto, deberás configurar el compartir archivos en las preferencias del sistema y posiblemente ajustar los permisos de red.

 

# Creación de subcarpetas en la carpeta Shared de macOS

## Objetivo

Crear las siguientes subcarpetas dentro de la carpeta `/Users/Shared`:

- personal
- trabajo
- wordpress
- prestashop
- academia
- a3erp
- borrar
- vscodeajustes
- arduino

## Comando

Para crear todas estas subcarpetas de una sola vez, puedes usar el siguiente comando `mkdir` con la opción `-p`:

```bash
mkdir -p /Users/Shared/{personal,trabajo,wordpress,prestashop,academia,a3erp,borrar,vscodeajustes,arduino}

```

## Explicación

- El comando `mkdir` se usa para crear directorios.
- La opción `p` permite crear directorios padres si no existen y no muestra errores si el directorio ya existe.
- Las llaves `{}` con las subcarpetas separadas por comas permiten crear múltiples directorios en una sola línea de comando.
- La ruta `/Users/Shared/` especifica dónde se crearán estas subcarpetas.

## Uso

1. Abre Terminal en tu Mac.
2. Copia y pega el comando anterior.
3. Presiona Enter para ejecutar el comando.

## Verificación

Después de ejecutar el comando, puedes verificar que las carpetas se han creado correctamente usando:

```bash
ls -l /Users/Shared

```

Esto mostrará una lista de todas las subcarpetas creadas dentro de `/Users/Shared`.

## Nota

Asegúrate de tener los permisos necesarios para crear carpetas en `/Users/Shared`. Si encuentras problemas de permisos, es posible que necesites usar `sudo` antes del comando `mkdir`.

# Creación y gestión de permisos de subcarpetas en /Users/Shared y añadir permisos en caso de fallos

## Creación de subcarpetas

Para crear las subcarpetas especificadas en /Users/Shared, utiliza el siguiente comando:

```bash
mkdir -p /Users/Shared/{personal,trabajo,wordpress,prestashop,academia,a3erp,borrar,vscodeajustes,arduino}

```

Este comando creará todas las subcarpetas en una sola operación.

## Permisos de las subcarpetas

Por defecto, las nuevas subcarpetas heredarán los permisos de la carpeta padre (/Users/Shared) si se han configurado correctamente las ACLs con la opción `file_inherit,directory_inherit`. Sin embargo, es importante verificar y, si es necesario, ajustar los permisos.

### Verificación de permisos

Para verificar los permisos de las nuevas subcarpetas:

```bash
ls -le /Users/Shared

```

Esto mostrará los permisos y ACLs de todas las subcarpetas.

### Ajuste de permisos (si es necesario)

Si los permisos no se han heredado correctamente, puedes ajustarlos con los siguientes comandos:

```bash
for dir in /Users/Shared/*; do
    sudo chmod 755 "$dir"
    sudo chown root:admin "$dir"
    sudo chmod +a "group:admin allow list,add_file,search,add_subdirectory,delete_child,readattr,writeattr,readextattr,writeextattr,readsecurity,file_inherit,directory_inherit" "$dir"
    sudo chmod +a "group:staff allow list,add_file,search,add_subdirectory,delete_child,readattr,writeattr,readextattr,writeextattr,readsecurity,file_inherit,directory_inherit" "$dir"
done

```

Este script realiza las siguientes acciones para cada subcarpeta:

1. Establece los permisos básicos (755)
2. Cambia el propietario a root y el grupo a admin
3. Añade ACLs para el grupo admin
4. Añade ACLs para el grupo staff (usuarios estándar del Mac)

## Verificación final

Después de aplicar los cambios, verifica nuevamente los permisos:

```bash
ls -le /Users/Shared

```

Esto debería mostrar que todas las subcarpetas tienen los mismos permisos y ACLs que la carpeta Shared principal.

## Nota importante

Recuerda que estos ajustes de permisos permiten el acceso a todos los usuarios del Mac a estas subcarpetas. Si necesitas permisos más restrictivos para carpetas específicas (por ejemplo, "personal"), considera ajustar los permisos individualmente para esas carpetas.

# Configuración Json del Git Project Manager (GPM) para reflejar la estructuras de la carpeta y subcarpetas /Users/Shared

# Configuracion del Json de Git Projet Manager para que use las carpetas de /Users/Shared/…

```jsx
{
  "gitProjectManager.baseProjectsFolders": [
    "/Users/Shared/personal",
    "/Users/Shared/trabajo",
    "/Users/Shared/wordpress",
    "/Users/Shared/prestashop",
    "/Users/Shared/academia",
    "/Users/Shared/a3erp",
    "/Users/Shared/borrar",
    "/Users/Shared/vscodeajustes",
    "/Users/Shared/arduino"
  ],
  "gitProjectManager.searchInsideProjects": true,
  "gitProjectManager.maxDepthRecursion": 2,
  "gitProjectManager.checkRemoteOrigin": true,
  "gitProjectManager.openInNewWindow": false,
  "gitProjectManager.storeRepositoriesBetweenSessions": true,
  "gitProjectManager.displayProjectPath": true,
  "gitProjectManager.warnIfFolderNotFound": true
}
```