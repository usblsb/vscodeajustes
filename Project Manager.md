Configurar la extensión Project Manager para Visual Studio Code basándote en la estructura de carpetas que has proporcionado. 

Project Manager es una extensión para Visual Studio Code que te ayuda a organizar y acceder fácilmente a tus proyectos, sin importar dónde estén ubicados. Sus principales características incluyen:

1. Guardar cualquier carpeta o espacio de trabajo como un proyecto.
2. Detectar automáticamente repositorios Git, Mercurial o SVN.
3. Organizar proyectos usando etiquetas.
4. Abrir proyectos en la misma ventana o en una nueva.
5. Identificar proyectos eliminados o renombrados.
6. Mostrar una barra de estado que identifica el proyecto actual.
7. Proporcionar una barra lateral dedicada.

Para configurar Project Manager según tus necesidades, te recomiendo lo siguiente:

1. Configurar las carpetas base:
   Añade las siguientes líneas a tu configuración de VS Code:

   ```json
   "projectManager.git.baseFolders": [
     "/Users/Shared/personal",
     "/Users/Shared/trabajo",
     "/Users/Shared/wordpress",
     "/Users/Shared/prestashop",
     "/Users/Shared/academia",
     "/Users/Shared/a3erp",
     "/Users/Shared/borrar",
     "/Users/Shared/vscodeajustes",
     "/Users/Shared/arduino"
   ]
   ```

   Esto hará que Project Manager busque proyectos Git en estas carpetas.

2. Configurar etiquetas:
   Puedes definir etiquetas personalizadas para organizar tus proyectos:

   ```json
   "projectManager.tags": [
     "Personal",
     "Trabajo",
     "WordPress",
     "Prestashop",
     "Academia",
     "A3ERP",
     "Arduino"
   ]
   ```

3. Otras configuraciones útiles:

   ```json
   "projectManager.sortList": "Name",
   "projectManager.groupList": true,
   "projectManager.showProjectNameInStatusBar": true,
   "projectManager.checkInvalidPathsBeforeListing": true,
   "projectManager.filterOnFullPath": true,
   "projectManager.removeCurrentProjectFromList": false
   ```

   Estas configuraciones ordenarán tus proyectos por nombre, los agruparán por tipo, mostrarán el nombre del proyecto en la barra de estado, verificarán rutas inválidas, permitirán filtrar por ruta completa y mantendrán el proyecto actual en la lista.

4. Si quieres que Project Manager detecte automáticamente proyectos de VS Code, puedes añadir:

   ```json
   "projectManager.vscode.baseFolders": [
     "/Users/Shared/personal",
     "/Users/Shared/trabajo",
     "/Users/Shared/wordpress",
     "/Users/Shared/prestashop",
     "/Users/Shared/academia",
     "/Users/Shared/a3erp",
     "/Users/Shared/borrar",
     "/Users/Shared/vscodeajustes",
     "/Users/Shared/arduino"
   ]
   ```

Con esta configuración, Project Manager escaneará automáticamente las carpetas especificadas en busca de proyectos Git y VS Code, te permitirá organizarlos con etiquetas personalizadas, y te proporcionará una forma fácil de acceder a ellos desde la barra lateral o la paleta de comandos de VS Code.