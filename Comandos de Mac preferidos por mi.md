# Comandos de Mac para Programadores

## Atajos de Teclado Generales

| Comando           | Descripción            |
| ----------------- | ---------------------- |
| `Cmd + C`         | Copiar                 |
| `Cmd + X`         | Cortar                 |
| `Cmd + V`         | Pegar                  |
| `Cmd + Z`         | Deshacer               |
| `Cmd + Shift + Z` | Rehacer                |
| `Cmd + A`         | Seleccionar todo       |
| `Cmd + F`         | Buscar                 |
| `Cmd + G`         | Buscar siguiente       |
| `Cmd + Shift + G` | Buscar anterior        |
| `Cmd + S`         | Guardar                |
| `Cmd + O`         | Abrir                  |
| `Cmd + W`         | Cerrar ventana         |
| `Cmd + Q`         | Salir de la aplicación |

## Atajos de Navegación

| Comando       | Descripción                                   |
| ------------- | --------------------------------------------- |
| `Cmd + Tab`   | Cambiar entre aplicaciones                    |
| `Cmd + ~`     | Cambiar entre ventanas de la misma aplicación |
| `Cmd + Space` | Abrir Spotlight                               |
| `Cmd + ,`     | Abrir preferencias de la aplicación actual    |

## Atajos para el Finder

| Comando                | Descripción              |
| ---------------------- | ------------------------ |
| `Cmd + N`              | Nueva ventana del Finder |
| `Cmd + Shift + N`      | Nueva carpeta            |
| `Cmd + Delete`         | Mover a la papelera      |
| `Cmd + Shift + Delete` | Vaciar papelera          |
| `Space`                | Vista previa rápida      |

## Atajos para Editores de Código

| Comando               | Descripción                 |
| --------------------- | --------------------------- |
| `Cmd + /`             | Comentar/Descomentar línea  |
| `Cmd + [`             | Indentar hacia la izquierda |
| `Cmd + ]`             | Indentar hacia la derecha   |
| `Cmd + Up`            | Ir al inicio del documento  |
| `Cmd + Down`          | Ir al final del documento   |
| `Option + Left/Right` | Moverse por palabras        |
| `Cmd + L`             | Seleccionar línea actual    |

## Comandos de Terminal

| Comando    | Descripción                                        |
| ---------- | -------------------------------------------------- |
| `Ctrl + C` | Cancelar el comando actual                         |
| `Ctrl + L` | Limpiar la pantalla                                |
| `Ctrl + A` | Mover el cursor al inicio de la línea              |
| `Ctrl + E` | Mover el cursor al final de la línea               |
| `Ctrl + U` | Borrar desde el cursor hasta el inicio de la línea |
| `Ctrl + K` | Borrar desde el cursor hasta el final de la línea  |

## Comandos para Fusionar Archivos

Cuando necesitas fusionar archivos y ya existen algunos en la carpeta de destino, puedes usar estos comandos en el Terminal:

### Usando `rsync`

```bash
rsync -av --update source_folder/ destination_folder/
```

- `-a`: modo archivo (copia recursivamente y preserva atributos)
- `-v`: modo verbose (muestra el progreso)
- `--update`: solo reemplaza archivos si la fuente es más reciente

### Usando `cp` con interactividad

```bash
cp -i source_folder/* destination_folder/
```

- `-i`: modo interactivo (pregunta antes de sobrescribir)

### Usando `ditto` (específico de Mac)

```bash
ditto -V source_folder destination_folder
```

- `-V`: modo verbose (muestra el progreso)

Estos comandos te pedirán confirmación antes de sobrescribir archivos existentes, permitiéndote decidir qué hacer en cada caso.

## Consejos Adicionales

- Usa `Tab` para autocompletar nombres de archivos y carpetas en el Terminal.
- El comando `man` seguido del nombre de otro comando te mostrará su manual de uso.
- Para ver el historial de comandos en el Terminal, usa `history`.

Recuerda que algunos atajos pueden variar dependiendo de la aplicación específica que estés usando. Siempre es buena idea consultar la documentación de tu editor o IDE preferido para conocer sus atajos específicos.
