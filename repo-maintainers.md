# Espacio de trabajo de Copilot para Mantenedores de Repositorios

El Espacio de trabajo de Copilot puede ayudarte como mantenedor de repositorio de varias formas:

1. El Espacio de trabajo de Copilot puede ayudarte a explorar soluciones potenciales para problemas.
2. El Espacio de trabajo de Copilot puede ayudarte a generar bocetos de soluciones para problemas, para posibles colaboradores, reduciendo la barrera de entrada.
3. El Espacio de trabajo de Copilot puede ayudar a fomentar una cultura en la que los creadores de problemas dejen notas adicionales útiles sobre cómo resolver problemas, para uso tanto de colaboradores como de asistentes de IA.

Por ejemplo, cuando se presenta un nuevo problema en tu repositorio, puedes usar el Espacio de trabajo de Copilot para generar un boceto de una solución para el problema. Luego puedes usar el botón "Compartir" para publicar este boceto en el hilo del problema, con comentarios adicionales sobre si crees que es útil o no, y dónde podría necesitar mejoras. Esto puede ayudar a los posibles colaboradores a comprender mejor el problema y proporcionar un punto de partida para su trabajo.

De manera similar, cuando se presenta un nuevo problema, puedes pedir al colaborador que cree una sesión en el Espacio de trabajo de Copilot para el problema. Esto puede ayudar al colaborador a comprender mejor el problema y proporcionar un punto de partida para su trabajo. También puedes incluir esta guía en la plantilla de problemas de tu repositorio, suponiendo que tus usuarios tengan acceso al Espacio de trabajo de Copilot. También puedes pedir a los colaboradores que dejen notas adicionales en la sesión del Espacio de trabajo de Copilot, lo cual puede ayudar a futuros colaboradores y asistentes de IA a comprender mejor el problema.

## Restringir el uso del Espacio de trabajo de Copilot en tu repositorio

Es posible que los colaboradores indisciplinados utilicen en exceso la generación de código asistida por IA. Debido a esto, ofrecemos a los mantenedores de repositorios la opción de deshabilitar el uso directo del Espacio de trabajo de Copilot para crear solicitudes de extracción y/o comentarios de problemas en sus repositorios.

Para deshabilitar la creación directa de solicitudes de extracción utilizando el Espacio de trabajo de Copilot, crea un archivo `.github/copilot-workspace/policy.json` en la rama predeterminada del repositorio que contenga el siguiente contenido:

```json
