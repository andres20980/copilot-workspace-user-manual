# Creación de Repositorios desde Plantillas

Copilot Workspace te permite crear repositorios a partir de plantillas utilizando lenguaje natural.

## Usando "Usar esta plantilla" desde GitHub.com

Para crear un repositorio con Copilot Workspace, puedes navegar hasta un repositorio de plantilla en GitHub.com y elegir "Usar esta plantilla", como se muestra a continuación:

<img src="images/creating-repos/create-repo-from-template.png" width=400 alt="Crear repositorio desde plantilla"><br>*Creando un repositorio desde una plantilla a través de Copilot Workspace*

La tarea se basa en la descripción del software a crear, además del LEEME del repositorio de plantilla. También puedes iniciar este tipo de tarea creando una [nueva sesión](#using-new-session-on-the-dashboard). Una vez iniciada una tarea de creación de repositorio, se verá así:

<img src="images/creating-repos/repo-task-timeline-representation.png" width=600 alt="Representación de la línea de tiempo de la tarea del repositorio"><br>*La tarea está etiquetada como "Repositorio" y el panel "Plantilla" indica el repositorio de plantilla*

Copilot Workspace generará una especificación para el repositorio basada en la descripción que proporciones, un plan para crearlo y finalmente la implementación final.

## Usando "Nueva sesión" en el panel de control

También puedes crear un repositorio a partir de una plantilla haciendo clic en el botón "Nueva sesión" en el [panel de control de Copilot Workspace](https://copilot-workspace.githubnext.com) y buscar una plantilla. Esto abrirá una nueva tarea en el espacio de trabajo donde puedes describir el software que deseas crear.

## Usando la URL

También puedes activar el modo "Crear Repositorio" para cualquier URL de repositorio agregando `?template=true` como parámetro de consulta. Por ejemplo:

https://copilot-workspace.githubnext.com/githubnext/hello-world?template=true

Para las URL entrantes, algunos repositorios se tratan como plantillas de forma predeterminada:

- Cualquier repositorio de plantilla de GitHub
- Cualquier repositorio en una organización que contenga `templates`, en mayúsculas o minúsculas, con guión al principio o al final
- Cualquier repositorio con `-template`, `-scaffold`, `-starter` o `-boilerplate` en su nombre, en mayúsculas o minúsculas, con guión al principio o al final
