# Consejos y Trucos

Este documento contiene varios consejos y trucos para utilizar Copilot Workspace de manera efectiva. ¡Nos encantaría conocer tus consejos y trucos también! Por favor, compártelos con nosotros en los [canales de retroalimentación](LEEME.md#feedback).

## Edita el Problema o Tarea

✨ CONSEJO: Puedes editar el problema o tarea para guiar a Copilot Workspace.

El panel de Problema/Tarea puede estar prellenado con contenido dependiendo de cómo ingresaste a Copilot Workspace. Por ejemplo, si comenzaste desde un Problema, el panel de Problema estará prellenado con el contenido del problema. Este contenido es efímero: las ediciones no se sincronizan de vuelta al problema, por lo que siéntete libre de editarlo para proporcionar más contexto o dirigir a Copilot Workspace hacia mejores resultados.

## ¡Las tareas pueden ser cortas!

✨ CONSEJO: Podrías sorprenderte de la efectividad de tareas simples como "Agregar pruebas unitarias"

Las tareas no tienen que ser largas. Declaraciones simples y claras de intención como "Cambiar a usar Python numpy" o "Agregar más pruebas unitarias para el código del servidor" pueden llevarte muy lejos. Puedes agregar fácilmente más aclaraciones e iterar.

## Aclara el Problema o Tarea

✨ CONSEJO: ¡Unas pocas palabras de aclaración pueden marcar una gran diferencia!

Solo unas pocas palabras de aclaración pueden marcar una gran diferencia en la calidad de los resultados que obtienes. Por ejemplo,

* _agregar pruebas unitarias correspondientes en `test/server`_ o

* _el problema está en el código de convolución_ o

* _no cambies ningún código existente, solo agrega pruebas unitarias_

son ejemplos de aclaraciones útiles. ¡Utiliza tantas de estas como desees!

## Considera utilizar Ejemplos

✨ CONSEJO: Dar ejemplos de lo que deseas puede ser una excelente manera de aclarar una tarea

Por ejemplo, puedes decir: _Aquí hay algunos ejemplos de invocaciones de línea de comandos que deberían funcionar después del cambio..._ y dar algunos ejemplos. O puedes decir: _Aquí hay algunos ejemplos de la salida esperada..._ y dar algunos ejemplos.

## Verifica el Tema y la Especificación

✨ CONSEJO: Verifica el tema y la especificación: si son precisos, entonces Copilot Workspace va por buen camino

El Tema es tu primer vistazo rápido al análisis de Copilot Workspace de tu tarea en el contexto de tu repositorio, y la Especificación Actual sigue poco después, luego la Especificación Actualizada. Si estas son precisas, entonces Copilot Workspace va por buen camino. Si no lo son, es posible que necesites proporcionar más contexto, aclaraciones e indicaciones en el panel de Problema/Tarea, o es posible que estés realizando algo más allá de las capacidades actuales de Copilot Workspace. Puedes editar todos estos para corregirlos y revisarlos rápidamente, lo cual puede ahorrarte mucho tiempo. También puedes retroceder y aclarar el problema o tarea y volver a intentarlo.

## Verificar la selección de contenido

✨ CONSEJO: Verifica la selección de contenido y utiliza notas breves en el problema o tarea para indicar dónde buscar

Puedes [verificar la selección de contenido utilizada](overview.md#content-selection). A menudo, la selección de contenido se puede mejorar y ahora mismo puedes hacerlo a través de lenguaje natural y notas en el panel de problema/tarea. Si sabes dónde está el código que necesita ser cambiado, puedes indicarlo en el panel de problema/tarea. Por ejemplo, puedes decir: _Mira en `src/server.js`_ u otras variaciones.

Para determinar cómo abordar una tarea, Copilot Workspace debe determinar qué archivos en un repositorio son relevantes para la tarea. Esto es difícil y Copilot Workspace no siempre seleccionará los archivos correctos. Si eso sucede, es posible que veas resultados de baja calidad.

Para revisar los archivos que se seleccionaron, en el panel de Especificación, haz clic en el botón "Ver referencias":

<img src="images/overview/references.png" width=600 alt="Mostrar cuadro de diálogo de referencias">

Para guiar a Copilot Workspace hacia una mejor selección de archivos, puedes mencionar nombres de archivos, nombres de directorios, etc. en el panel de problema/tarea. Solo escríbelo de forma natural, como si estuvieras escribiendo un problema normal.

## Si al principio no tienes éxito...

✨ CONSEJO: Intenta regenerar la especificación o el plan

Si no estás satisfecho con los resultados que estás obteniendo, puedes intentar regenerar la especificación y/o el plan. Para hacer esto, haz clic en el botón "Regenerate" en los paneles de Especificación o Plan:

<img src="images/tips-and-tricks/regen.png" width=600 alt="Botón Regenerate">

## Iterar en la implementación

✨ CONSEJO: Agrega notas breves a los archivos en el plan, luego itera

A menudo, Copilot Workspace obtendrá una tarea *casi correcta*, pero puede tener problemas con algunas partes. En este caso, puedes reimplementar archivos específicos con instrucciones nuevas o adicionales. Después de implementar y revisar el código, puedes seleccionar archivo(s) en el panel de Plan y agregar viñetas, luego hacer clic en "Update selected files" para reimplementar esos archivo(s) con las nuevas instrucciones que has proporcionado.

<img src="images/overview/file-iteration.png" width=600 alt="Flujo de actualización de archivos seleccionados">

## Agregar nuevos archivos e iterar

✨ CONSEJO: Puedes agregar nuevos archivos e iterar en la implementación

Si necesitas agregar nuevos archivos a la implementación, puedes hacerlo haciendo clic en el botón "Add file" en el panel de Plan. Esto agregará un nuevo archivo al plan, que luego puedes implementar e iterar.

## Considera generar nuevos archivos

✨ CONSEJO: Generar nuevos archivos puede ser mejor que agregar a archivos existentes

Esta vista previa técnica de Copilot Workspace utiliza "rewriting de archivo completo". Esto significa que cuando le pides a Copilot Workspace que agregue código a un archivo, reemplazará todo el archivo con el nuevo código. Al realizar tareas como escribir pruebas unitarias o generar documentación o código de implementación nuevo, puede ser más fácil y rápido generar nuevos archivos y luego renombrarlos.

## Comparte temprano, comparte a menudo

✨ CONSEJO: Puedes compartir tu sesión en cualquier momento, incluso con personas que no forman parte de la vista previa de Copilot Workspace.

Puedes compartir tu sesión de Copilot Workspace con otras personas haciendo clic en el botón "Share" en la esquina superior derecha de la pantalla. Esto generará un enlace que puedes compartir con otros. Estos enlaces se pueden compartir con invitados, incluso si no forman parte de la vista previa de Copilot Workspace. Deberán iniciar sesión con su cuenta de GitHub para ver la sesión.

Las sesiones compartidas son copias de la sesión original. Los usuarios que no sean invitados pueden usarlas como punto de partida para continuar la tarea o explorar soluciones alternativas sin interferir con la sesión original. Los usuarios invitados pueden ver la sesión pero no pueden usar el espacio de trabajo para realizar cambios.

<img src="images/overview/share-link.png" width=200 alt="Botón Share">

## Utiliza las sesiones

✨ CONSEJO: Vuelve a tu trabajo en cualquier momento

Tus sesiones se guardan automáticamente, por lo que no perderás el trabajo si cierras el navegador o te alejas de la página. Puedes volver a tu sesión yendo a [tu panel de Copilot Workspace](https://copilot-workspace.githubnext.com).

## Configura la terminal para tu repositorio

✨ CONSEJO: Configura un archivo `devcontainer.json` en tu repositorio para configurar la terminal

Proporcionamos una terminal incorporada para que puedas validar los cambios de código que Copilot Workspace sugiere. Utilizamos GitHub Codespaces para proporcionar esta terminal y usamos el archivo `devcontainer.json` en tu repositorio para configurar el contenedor que alimenta la terminal. Si necesitas hacer cambios en el contenedor predeterminado, como instalar software necesario, etc., puedes hacerlo creando un archivo `devcontainer.json` en tu repositorio. Obtén más información sobre los contenedores de desarrollo en https://containers.dev/.

## Utiliza el Codespace

✨ CONSEJO: La edición completa en el Codespace es simple y rápida

Los archivos modificados se sincronizan en ambas direcciones entre Copilot Workspace y la terminal/Codespace. Siéntete libre de editar en cualquier lugar y los cambios se reflejarán en el otro.

Consulta [Guía de Codespaces](./codespaces-guide.md) para obtener más información.

## ¡Explora los Experimentos!

✨ CONSEJO: ¡Explora nuestros experimentos y envíanos comentarios!

Siempre estamos probando cosas nuevas en Copilot Workspace. Puedes optar por participar en nuestros experimentos actuales haciendo clic en tu avatar en la esquina superior derecha de la pantalla y seleccionando "Experimentos":

<img src="images/tips-and-tricks/experiments.png" width=200 alt="Selector de Experimentos">

## Trabajar con la "pereza" del modelo

✨ CONSEJO: Si el modelo es "perezoso" y omite partes de los archivos editados, copia y pega las partes faltantes desde la diferencia

A veces, el modelo será "perezoso" y omitirá partes de los archivos editados. Si ves que esto sucede, puedes copiar las partes faltantes del lado izquierdo de la diferencia y pegarlas en el lado derecho. Sabemos que esto no es ideal y estamos trabajando arduamente en este problema.

## Editar código en Copilot Workspace

✨ CONSEJO: Edita directamente en los editores de código por archivo en Copilot Workspace

Cuando Copilot Workspace ha generado una sugerencia, se te presenta en el panel de implementación. ¡Pero esas sugerencias no son solo de lectura! Puedes editarlas y hacer cambios según desees.

<img src="images/tips-and-tricks/code-editor.png" width=300 alt="Editar código en Copilot Workspace">

Y si tienes un GitHub Codespace abierto, ¡esas ediciones se sincronizarán entre Copilot Workspace y el GitHub Codespace también!

## ¿Necesitas volver atrás?

✨ CONSEJO: Puedes usar los botones de deshacer y rehacer para viajar entre un estado anterior y más nuevo de tu espacio de trabajo.

Puedes usar los botones de deshacer y rehacer para volver a un estado anterior de tu espacio de trabajo. Esto puede incluir revertir una implementación o las adiciones y ajustes que hayas realizado en tu especificación o plan.

<img src="images/tips-and-tricks/undo-redo.png" width=300 alt="Usar deshacer y rehacer para cambiar estados en Copilot Workspace">

## ¿En movimiento? Prueba Copilot Workspace en tu móvil

✨ CONSEJO: Copilot Workspace es compatible con dispositivos móviles, ¡así que considera hacer cambios sobre la marcha!

Las ideas pueden surgir en cualquier lugar, ya sea en tu escritorio, en una cafetería o en un autobús. ¡Con esa chispa de creatividad, puedes usar Copilot Workspace desde tu móvil para explorar ideas! Y si no completaste completamente tu tarea, puedes usar el panel de control en Copilot Workspace para retomar donde lo dejaste.

Y si deseas acceder fácilmente a Copilot Workspace en cualquier momento, puedes agregarlo a la pantalla de inicio de tu móvil siguiendo estos pasos:

1. Abre tu navegador móvil y ve al panel de control de Copilot Workspace en [https://copilot-workspace.githubnext.com](https://copilot-workspace.githubnext.com).
2. Una vez que se cargue el panel de control, toca el menú del navegador y selecciona "Agregar a la pantalla de inicio" para acceder fácilmente a Copilot Workspace desde tu pantalla de inicio.
3. Confirma la acción si se te solicita y Copilot Workspace se agregará a tu pantalla de inicio, brindando una experiencia similar a una aplicación nativa gracias al soporte de PWA.

## Recuperar el acceso si revocaste OAuth

Copilot Workspace se implementa como una aplicación OAuth. Si revocaste la autorización de la aplicación en la configuración de tu cuenta de GitHub, ya no podrás usar Workspace. Puedes restaurar tu acceso en https://copilot-workspace.githubnext.com/ cerrando sesión, luego iniciando sesión y volviendo a autorizar la aplicación OAuth.

## Enlaces entrantes

✨ CONSEJO: Copilot Workspace tiene la capacidad de especificar la tarea mediante parámetros de consulta cuando el tema es un repositorio, una rama o una solicitud de extracción.
