# Preguntas Frecuentes sobre IA Responsable

## ¿Qué es Copilot Workspace?

Copilot Workspace es un bucle interno de desarrollo reinventado. Los puntos focales de la experiencia son seleccionar una tarea, expresar la intención y luego colaborar con la IA hacia una solución. Creemos que esto puede reducir drásticamente la complejidad, mejorar la productividad y deleitar a los desarrolladores, sin eliminar los aspectos del desarrollo de software que más valoran, como la toma de decisiones, la creatividad y la propiedad.

## ¿Qué puede hacer Copilot Workspace?

Copilot Workspace recibe una tarea de desarrollo de un usuario, por ejemplo, un problema de GitHub, y produce una especificación en lenguaje natural del comportamiento actual del código, un plan sobre cómo modificar el código para completar la tarea y, finalmente, los cambios reales en los archivos relevantes del repositorio. Cada paso (tarea, especificación, plan e implementación) es editable por el usuario, lo que le permite guiar a la IA para completar la tarea de la mejor manera posible.

## ¿Cuál(es) es/son el(los) uso(s) previsto(s) de Copilot Workspace?

Copilot Workspace tiene como objetivo:

1. Acelerar a los desarrolladores de software, ayudándoles a realizar cambios de código pequeños y medianos de manera rápida y correcta.
2. Reducir la energía de activación para que los desarrolladores inicien tareas, brindándoles un punto de partida generado por IA.
3. Ayudar a los desarrolladores experimentados a trabajar con lenguajes de programación y marcos de trabajo desconocidos.
4. Ayudar a los desarrolladores a contribuir en bases de código desconocidas, por ejemplo, en proyectos de código abierto.

## ¿Cómo se evaluó Copilot Workspace? ¿Qué métricas se utilizan para medir el rendimiento?

Copilot Workspace se evaluó de las siguientes maneras:

* Evaluaciones sin conexión. Tenemos un corpus de tareas conocidas y un punto de entrada que nos permite ejecutar Copilot Workspace en modo sin cabeza sobre esas tareas. Cuando realizamos cambios en nuestras indicaciones, cambiamos a un modelo diferente, etc., ejecutamos esas pruebas y validamos manualmente los cambios en las salidas de Copilot Workspace. Si encontramos regresiones, iteramos en las indicaciones hasta que no haya más regresiones. Además, tenemos un conjunto más grande de pruebas que se extraen de GitHub, y utilizamos evaluaciones basadas en modelos para garantizar una calidad consistente.
* Estudios de usuarios. En enero, realizamos una serie de estudios de usuarios con empleados de GitHub, donde les dimos una tarea estándar y les pedimos que completaran la tarea utilizando Copilot Workspace. Estamos planeando estudios de usuarios adicionales como parte de la Vista previa técnica.
* Uso intensivo dentro de nuestro equipo. Utilizamos Copilot Workspace para construir Copilot Workspace.
* Evaluación por parte de un equipo de seguridad. Hemos preparado un conjunto de indicaciones maliciosas y hemos ejecutado Copilot Workspace en modo sin cabeza sobre esas indicaciones. Luego, realizamos evaluaciones tanto humanas como basadas en modelos de las salidas en busca de respuestas dañinas, y si encontramos alguna, actualizamos nuestras indicaciones y filtros para que los usuarios no las encuentren.

## ¿Cuáles son las limitaciones de Copilot Workspace? ¿Cómo pueden los usuarios minimizar el impacto de las limitaciones de Copilot Workspace al utilizar el sistema?

Copilot Workspace no siempre es correcto. Los usuarios deben validar cuidadosamente su salida y no confiar ciegamente en ella. Si los usuarios detectan inexactitudes en las salidas de Copilot Workspace, les hemos facilitado la edición y corrección de cualquier salida generada por el modelo. También hemos construido herramientas de validación, en particular una terminal que permite al usuario ejecutar el código generado en un entorno aislado. El usuario debe utilizar estas herramientas para validar y corregir las salidas de Copilot Workspace.

## ¿Qué factores operativos y configuraciones permiten un uso efectivo y responsable de Copilot Workspace?

Copilot Workspace funcionará mejor en lenguajes de programación y marcos de trabajo comunes y cuando el lenguaje natural sea el inglés.

El código generado por Copilot Workspace debe cumplir con el mismo estándar que el código escrito por humanos: debe ser revisado, tener pruebas automatizadas, ser analizado por linters y analizadores estáticos, etc. Copilot Workspace puede ayudar a agregar pruebas automatizadas a las solicitudes de extracción en curso, lo que ayuda a mejorar la salud general de un proyecto de software.

## ¿Qué debe hacer un usuario si encuentra contenido ofensivo mientras usa Copilot Workspace?

Por favor, informe cualquier ejemplo de contenido ofensivo a copilot-safety@github.com. Por favor, incluya un enlace compartido para que podamos investigar.
