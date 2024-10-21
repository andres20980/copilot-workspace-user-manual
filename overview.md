# Copilot Workspace: Descripción General

[Copilot Workspace](https://githubnext.com/projects/copilot-workspace/) es un asistente de IA centrado en tareas. Cada día como desarrollador comienzas con una tarea y emprendes el viaje para explorar, comprender, refinar y completar esa tarea, un viaje que puede ser emocionante, desafiante, fascinante y gratificante. Copilot Workspace te acompaña en cada paso de este viaje, desde la tarea hasta el código funcional.

Copilot Workspace se basa en un conjunto de principios que guían su diseño y desarrollo:

* Copilot Workspace es _contextual_. Está profundamente integrado con GitHub y es consciente del contexto de tu tarea: el repositorio, el problema, la solicitud de extracción.

* Copilot Workspace es _asistente_. Ofrece un lienzo para que navegues por tareas desconocidas, mejorando tus habilidades de desarrollo con un nuevo tipo de asistencia de IA.

* Copilot Workspace es _omnipresente_. Está listo y esperando por ti, disponible en cada problema de cada repositorio habilitado en GitHub. Y Copilot Workspace incluso está ahí para ti al comenzar un nuevo código, disponible en cada repositorio de plantillas para crear nuevo software utilizando lenguaje natural.

* Copilot Workspace es _iterativo_. Copilot Workspace te anima a verificar, revisar, refinar e iterar en las salidas generadas por IA. Tú, como desarrollador, tienes el control.

* Copilot Workspace es _colaborativo_. Puedes compartir sesiones con tu equipo y publicar enlaces a tus sesiones en problemas y solicitudes de extracción. Y si eres el mantenedor de un repositorio, te brindamos controles para ayudarte a gestionar el uso del desarrollo asistido por IA en tus repositorios.

* Copilot Workspace es _configurable_. Puedes integrar Copilot Workspace en tus flujos de trabajo a través de enlaces profundos a Copilot Workspace que especifican tareas comunes.

En este manual, te guiaremos a través de los conceptos y características de Copilot Workspace y te ayudaremos a comenzar a utilizarlo de manera efectiva.

<img src="images/overview/session.png" width="600" alt="Una sesión de espacio de trabajo completamente implementada">

*Una sesión de espacio de trabajo completamente implementada*

## Características

1. [Tarea](#tarea)
1. [Especificación](#especificación)
1. [Plan](#plan)
1. [Implementación](#implementación)
1. [Iteración de archivos](#iteración-de-archivos)
1. [Terminal integrada](#terminal-integrada)
1. [Compartir sesión](#compartir-sesión)
1. [Finalización de tarea](#finalización-de-tarea)
1. [Panel de sesión](#panel-de-sesión)

## Tarea

Todo en Copilot Workspace comienza con una "tarea", que es una descripción en lenguaje natural de la intención. La tarea siempre tiene un contexto: un repositorio de GitHub.
Para esta vista previa técnica, Copilot Workspace admite cuatro tipos de tareas: resolver problemas, [refinar solicitudes de extracción](pull-request-tasks.md), [crear repositorios a partir de plantillas](creating-repos.md) y [tareas ad hoc](adhoc-tasks.md). Aquí nos enfocamos en resolver problemas, que son el punto de entrada más común.

Una vez inscrito en la vista previa técnica, en cada problema de GitHub encontrarás un nuevo botón "Abrir en Workspace":

<img src="images/general/open-in-workspace.png" width=400 alt="Botón en la página del problema para abrir en Copilot Workspace">

*Abre un problema en Copilot Workspace*

Esto abrirá Copilot Workspace contextualizado a este problema. Para las tareas de problema, la tarea se basa en el título y el cuerpo del problema, además del hilo de comentarios del problema. Copilot Workspace avanzará inmediatamente al siguiente paso en la línea de tiempo. Esto se ve así:

<img src="images/overview/issue-timeline-representation.png" width=600 alt="Representación de la línea de tiempo de la tarea del problema">

*La tarea está etiquetada como "Problema" y comienza el análisis*

## Especificación

Para ayudar a resumir una definición de tarea no trivial (por ejemplo, un problema con un hilo de comentarios largo), Copilot Workspace primero genera un "tema" para la tarea, que toma la forma de una pregunta que se puede plantear contra el código base y se utiliza para definir los criterios de éxito antes/después (ver la sección de [especificación](#especificación) a continuación).
<img src="images/overview/topic-question.png" width=600 alt="Pregunta del tema">

*Observa cómo el tema introduce claridad que está completamente ausente en el título del problema*

Puedes pensar en el tema como una forma de destilar la tarea a su esencia y darte la oportunidad temprana y rápida de ver si Copilot Workspace va por buen camino. Si el tema es incorrecto, no necesitas continuar. Pero si el tema es correcto, te ayuda a comprender mejor la tarea y a centrarte en los aspectos más importantes del código que son relevantes para la tarea.

Después de producir el tema, Copilot Workspace genera una lista con viñetas que describe el comportamiento actual del código, basado en la tarea y el tema planteados. Esto ayuda a aumentar tu confianza de que Copilot Workspace va por buen camino y sirve como una forma de incorporarte al contexto, en casos en los que es posible que no comprendas completamente el estado actual.

<img src="images/overview/current-spec.png" width=600 alt="Especificación actual">

*La especificación actual responde a la pregunta del tema basada en el estado actual*

Y si Copilot Workspace se equivoca en algo, puedes editar o eliminar pasos de la especificación actual, o incluso elegir generar una especificación completamente nueva ("intentar de nuevo"). En la práctica, encontramos que suelen ser bastante buenas en el primer intento.
Después de la especificación actual, Copilot Workspace genera una "especificación propuesta", que es una lista con viñetas que articula el estado en el que estaría el código después de resolver la tarea (respondiendo efectivamente a la pregunta del tema). Y en particular, la especificación propuesta se centra en definir los criterios de éxito de la tarea, en lugar de entrar en detalles de implementación (que es el papel del [plan](#plan)).

<img src="images/overview/proposed-spec.png" width=600 alt="Especificación propuesta">

*La especificación propuesta indica cómo editar el código para resolver la tarea*

## Selección de contenido

Para generar las especificaciones actuales y propuestas, y para todos los pasos posteriores, Copilot Workspace necesita identificar qué archivos en el código son relevantes para comprender y completar la tarea. Esto se logra mediante una combinación de técnicas de LLM y búsqueda de código tradicional. El contenido de los archivos con mayor ranking se utiliza como contexto para casi todos los pasos en el flujo de trabajo.

Los usuarios pueden revisar los archivos seleccionados por Copilot Workspace utilizando el botón "Ver Referencias" en el panel de Especificaciones. Para ajustar qué archivos se seleccionan, los usuarios pueden editar la tarea y utilizar lenguaje natural para especificar qué archivos son relevantes.

<img src="images/overview/references.png" width=600 alt="Mostrar cuadro de diálogo de referencias">

*Las referencias que el modelo utilizó para generar las especificaciones originales y modificadas*

## Plan

Una vez que estés satisfecho con las especificaciones actuales y propuestas, puedes solicitar a Copilot Workspace que genere un plan, que es una lista de los archivos que deben modificarse (por ejemplo, editarse, crearse, eliminarse, moverse o renombrarse) para lograr los criterios de éxito de la especificación propuesta. Además, cada archivo modificado incluye una lista de pasos específicos que indican los cambios exactos que deben realizarse.

Al igual que la especificación, el plan es completamente editable y se puede regenerar, lo que te permite refinar y guiar a Copilot Workspace en la dirección correcta.

<img src="images/overview/plan.png" width=600 alt="Plan">

*Un plan que muestra los pasos necesarios para editar un archivo y agregar otro*

## Implementación

Cuando estés satisfecho con el plan, puedes hacer clic en el botón "Implementar" para comenzar a implementarlo. Esto actualizará la interfaz de usuario para mostrar una serie de actualizaciones de archivos en cola en el lado derecho, y luego comenzará a generar el contenido actualizado de los archivos uno por uno. Cuando un archivo comienza a generarse, su entrada asociada en el plan mostrará que está en progreso. Y cuando se completa, el plan indicará que está terminado.

Una vez que se implementa un archivo, Copilot Workspace muestra una vista de diferencias para él y se desplaza automáticamente al primer cambio. Los editores de diferencias son editables, lo que permite realizar ajustes menores directamente en el código, en lugar de iterar a través de cambios en la tarea, especificación o plan.

## Iteración de archivos

Copilot Workspace no siempre acierta en todo, por lo que facilita a los usuarios iterar en los archivos de implementación uno por uno. Simplemente agrega, elimina o edita elementos en los pasos del plan para cada archivo, marca la casilla de verificación y haz clic en el botón "Actualizar archivos seleccionados". Esto regenerará el contenido de los archivos seleccionados y actualizará la vista de diferencias.

Por ejemplo, puedes editar directamente la diferencia, o puedes volver al plan y hacer cambios allí. Y si necesitas hacer cambios más extensos, puedes regenerar completamente el plan.

<img src="images/overview/file-iteration.png" width=600 alt="Panel de plan con iteración de archivos">

*El panel de plan permite a los usuarios iterar en la implementación archivo por archivo*

## Terminal integrada

Una vez que hayas implementado el plan, Copilot Workspace te permite validar los cambios para verificar su corrección mediante la apertura de una terminal integrada y la ejecución de comandos de shell. Esto permite compilar, analizar, probar, etc. los cambios, y puede ser una forma rápida y efectiva de ganar confianza sobre la tarea y su estado de finalización. La terminal está respaldada por un Codespace, por lo que es un entorno de desarrollo seguro con un entorno de desarrollo completo instalado.

<img src="images/overview/terminal.png" width=600 alt="Terminal integrada">

*Terminal integrada, mostrando el nombre de la rama generada y acceso a la informática justo a tiempo*

Si necesitas hacer cambios más extensos o aprovechar las funciones avanzadas del editor (por ejemplo, depuración paso a paso), puedes abrir la sesión de Copilot Workspace en un Codespace, utilizando cualquiera de los clientes admitidos por Codespace.

## Compartir sesión

Para facilitar el uso compartido de una sesión de espacio de trabajo con otros (por ejemplo, para revisar el código de forma ad hoc o compartir una idea de implementación inicial), Copilot Workspace permite a los usuarios generar enlaces compartidos. Estos enlaces se pueden compartir con invitados, incluso si no forman parte de la vista previa de Copilot Workspace.

Las sesiones compartidas son copias de la sesión original. Los usuarios no invitados pueden utilizarlas como punto de partida para continuar la tarea o explorar soluciones alternativas sin interferir con la sesión original. Los usuarios invitados pueden ver la sesión pero no pueden realizar cambios en el espacio de trabajo.

<img src="images/overview/share-link.png" width=600 alt="Generar un enlace compartido">

*Generando un enlace compartido desde la barra de encabezado*

Cuando trabajas con problemas y solicitudes de extracción, también puedes:

* Publicar un comentario en un problema. Copilot Workspace genera automáticamente un comentario con un enlace compartido a la sesión, que se incluye en el problema. Esto permite a los revisores acceder rápidamente a la sesión del espacio de trabajo y ver los cambios propuestos.

* Publicar un comentario en una solicitud de extracción. Similar al comentario del problema, Copilot Workspace genera automáticamente un comentario con un enlace compartido a la sesión, que se incluye en la solicitud de extracción. Esto permite a los revisores acceder rápidamente a la sesión del espacio de trabajo y ver los cambios propuestos.

## Finalización de la tarea

Cuando una tarea se implementa, valida y revisa, puedes completar la tarea de diferentes formas, según el tipo de tarea en la que estés trabajando.

<img src="images/overview/task-completion.png" width=600 alt="Crear una solicitud de extracción">

*Creando una solicitud de extracción para los cambios implementados*

| Tipo de tarea | Completaciones disponibles | 
|---------------| ------------------------ |
| Problema | — Crear solicitud de extracción <br> — Crear solicitud de extracción en borrador <br> — Hacer push a una nueva rama <br> — Hacer cambios en la rama actual (solo disponible si tienes permisos de confirmación en el repositorio) <br> <br> Estas acciones pueden bifurcar el repositorio si no tienes permisos de escritura |
| Tarea ad hoc | — *Igual que para problemas* |
| Tarea de solicitud de extracción | — Actualizar solicitud de extracción (hace un nuevo commit con los cambios) <br> — *Igual que para problemas* |
| Tarea de repositorio | — Crear repositorio (crea un nuevo repositorio a partir del repositorio de plantilla seleccionado e incluye los cambios) |

## Panel de sesión

Copilot Workspace guarda automáticamente tu trabajo. También proporciona un panel de sesión, que te permite reanudar fácilmente tu trabajo más tarde. Puedes comenzar una tarea desde tu teléfono y luego terminarla en tu computadora portátil, o viceversa.

<img src="images/general/dashboard.png" width=600 alt="Panel de Copilot Workspace">

*El panel de Copilot Workspace muestra sesiones recientes, marcadas y completadas*

La funcionalidad de deshacer y rehacer es compatible dentro de la sesión a través de botones en la barra de herramientas.

## Apéndice: Glosario

| Término | Definición |
|---------|------------|
| Copilot Workspace | Un entorno de desarrollo nativo de Copilot diseñado para explorar y completar tareas diarias |
| Objetivo | Una rama de código en un commit específico |
| Tarea | Una descripción en lenguaje natural de un cambio en un objetivo |
| Tema | Una breve frase de resumen de una tarea, generalmente en forma de pregunta |
| Especificación | Una descripción del estado actual y propuesto del objetivo en relación con la tarea |
| Plan | Una lista de archivos para agregar, eliminar o cambiar, con notas sobre cada uno de ellos, que juntos transforman el objetivo desde su estado actual a su estado propuesto |
| Implementación | Un conjunto de cambios en el objetivo que, cuando se aplican, completan la tarea |
| Sesión | El progreso guardado de un usuario hacia la finalización de una tarea, una sola tarea puede tener muchas sesiones |
| Sesión de instantánea | Una instantánea de la sesión de un usuario, creada cuando haces clic en "Compartir enlace", que incluye tanto el progreso de la tarea como el estado de la interfaz de usuario |
