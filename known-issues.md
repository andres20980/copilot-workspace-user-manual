# Problemas Conocidos y Mejoras Futuras

Recuerda que Copilot Workspace es una vista previa técnica y es un área de desarrollo activo. Este documento enumera algunos problemas conocidos y áreas conocidas en las que nos gustaría realizar mejoras futuras del producto.

A continuación se presentan áreas principales en las que estamos trabajando activamente para mejorar Copilot Workspace.

### Reescritura de archivos grandes

Cuando Copilot Workspace implementa un plan que implica cambios en un archivo grande, puede llevar mucho tiempo completarlo. Copilot Workspace utiliza actualmente la "reescritura de archivo completo" ya que hemos encontrado que esto logra un alto nivel de exhaustividad en la amplia gama de tareas heterogéneas para las que se puede utilizar Copilot Workspace.

Estamos trabajando en técnicas de reescritura parcial de archivos, tanto automáticas como con la guía del usuario, para mejorar el rendimiento de esta operación.

### Generación de código

La calidad del código generado por Copilot Workspace no siempre es perfecta. Está altamente relacionada con la calidad de los modelos de IA subyacentes utilizados. Estamos trabajando en mejorar la calidad del código generado por Copilot Workspace en muchos niveles.

Por ejemplo, la calidad de la generación de código se ve afectada por la calidad de la planificación y especificación de la tarea, y la experiencia general del usuario al evaluar y aclarar estos aspectos. Estamos trabajando para mejorar esto también.

La calidad lograda también está relacionada con la experiencia de iterar en el código generado. Estamos analizando técnicas de iteración más detalladas.

### Selección de contenido

La selección de contenido en Copilot Workspace a veces puede ser subóptima, lo que lleva a la generación de código que no es relevante para la tarea. Estamos trabajando en mejorar la selección de contenido en Copilot Workspace.

### Recuperación web

Las tareas pueden incluir enlaces directos a recursos web como documentación. Además, algunas recuperaciones web también se pueden deducir de la tarea. Copilot Workspace actualmente no realiza recuperación web y estamos trabajando en agregar esta función.

### Reparación de compilación/prueba

Después de generar el código, tanto la IA como las herramientas tradicionales pueden usarse para "reparar" el código en función de los diagnósticos generados a partir de la compilación, prueba y ejecución del código. Ya tenemos cierto soporte para esto en Copilot Workspace y estamos trabajando en mejorarlo.

### Tareas pequeñas, tareas grandes

Algunas tareas son muy pequeñas: actualizar algunas líneas de un archivo. Algunas tareas son muy grandes: implementar una nueva característica completa de un repositorio.

Copilot Workspace está diseñado actualmente para el rango medio de tareas típicas de los problemas de GitHub. Estamos interesados en ofrecer variaciones de los conceptos principales de Copilot Workspace en disposiciones más adecuadas para tareas pequeñas y grandes. Por ejemplo, para tareas pequeñas podemos ofrecer una versión "lite" de Copilot Workspace donde solo está la tarea. Para tareas grandes podemos ofrecer una forma de descomponer la tarea en sub-tareas.

### Autorización

Copilot Workspace utiliza una aplicación OAuth de GitHub para la autenticación. Algunas organizaciones pueden tener [políticas que restringen las aplicaciones OAuth para interactuar con sus repositorios](https://docs.github.com/en/organizations/managing-oauth-access-to-your-organizations-data/about-oauth-app-access-restrictions). No podrás realizar tareas en repositorios privados con Copilot Workspace, ni crear solicitudes de extracción en repositorios públicos a menos que el administrador de la organización apruebe la aplicación OAuth de Copilot Workspace.

Estamos trabajando en agregar una segunda opción de autorización para Copilot Workspace basada en una aplicación de GitHub, y actualizaremos este documento cuando esté disponible.

### Escalabilidad

Copilot Workspace se puede utilizar con muchos repositorios grandes existentes. Sin embargo, algunos repositorios son tan grandes que incluso listar sus archivos puede ser un ejercicio desafiante. Además, algunos repositorios contienen contenido muy inusual: archivos con líneas enormemente largas o archivos binarios con extensiones inusuales, entre otros. Los repositorios grandes también presentan desafíos para la selección de contenido y la planificación.

Copilot Workspace establece un límite en el tamaño de los repositorios informado por GitHub que se pueden analizar. Si un repositorio está por encima de este límite, es posible que veas `Copilot Workspace may not be used to analyze <owner>/<repo> due to size limitations`.

Estamos trabajando en mejorar la escalabilidad de Copilot Workspace para manejar estos casos.

### Validación

Copilot Workspace proporciona una terminal integrada para ayudar con la validación del código. Estamos trabajando continuamente en una variedad de técnicas para mejorar las capacidades de validación de Copilot Workspace.

### Herramientas para desarrolladores

Copilot Workspace se entrega actualmente como una aplicación web con una modalidad de experiencia de usuario concreta. Un principio de diseño fundamental es hacer que esta experiencia esté disponible de manera generalizada, y evaluaremos la posibilidad de habilitar mecanismos de entrega alternativos en IDE o en la línea de comandos.

También estamos considerando ampliar la gama de herramientas para desarrolladores para integrarse con la experiencia web de Copilot Workspace.

## Problemas conocidos

A continuación se presentan problemas conocidos más específicos relacionados con la versión actual de Copilot Workspace.

### Detección de ambigüedad puede activarse con demasiada frecuencia

La detección de ambigüedad en Copilot Workspace a veces puede ser demasiado sensible y puede activarse incluso cuando la tarea es clara. Estamos trabajando en mejorar la precisión de la detección de ambigüedad en Copilot Workspace.

### La selección de una tarea existente necesita una mejor experiencia de usuario

Al seleccionar una tarea existente en la que trabajar, la experiencia de usuario no es tan fluida como podría ser, y puede ser más fácil ajustar el enlace profundo URL para Copilot Workspace o volver a la página de la tarea en GitHub y elegir "Abrir en Workspace".

### Los commits de las solicitudes de extracción de Workspaces no están firmados actualmente

Los commits de las solicitudes de extracción de Workspaces no están firmados actualmente. Estaremos trabajando en agregar esta función.

### No hay un botón de "Detener" al generar descripciones de solicitudes de extracción

No hay un botón de "Detener" al generar descripciones de solicitudes de extracción. Estamos trabajando en agregar esta función.

### La lista de autocompletado a veces se posiciona incorrectamente en dispositivos móviles

En dispositivos móviles, la lista de autocompletado se posiciona incorrectamente al agregar un archivo al plan. Se está trabajando en una solución para esto.

### Tiempo de inicio de la terminal

Estamos trabajando activamente en mejorar el tiempo de inicio de la terminal en Copilot Workspace.

### Tiempo de espera del botón de ayuda de la terminal

El flujo de reparación desde la terminal al plan a veces se agota, lo que hace que el botón de ayuda de la terminal indique que no puede ayudarte. 
Una solución alternativa para esto es hacer clic en el botón de enviar (icono de flecha hacia arriba) nuevamente para regenerar la sugerencia.
Entendemos que esto no es ideal y estamos trabajando en una solución para este problema.
