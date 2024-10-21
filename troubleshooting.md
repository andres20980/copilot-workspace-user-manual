## Solución de Problemas

### Introducción

¡Bienvenido a la guía de solución de problemas de Copilot Workspace! En esta sección, te proporcionaremos consejos útiles y soluciones a problemas comunes que puedes encontrar al trabajar con organizaciones y repositorios privados en Copilot Workspace. Nuestro objetivo es asegurarnos de que tengas una experiencia fluida y productiva. ¡Vamos a sumergirnos!

### Solución de Problemas con Organizaciones

Cuando trabajas con organizaciones en Copilot Workspace, es posible que encuentres algunos problemas comunes. Aquí tienes algunos consejos de solución de problemas para ayudarte a resolverlos:

- **Estás accediendo a una organización que debe aprobar las aplicaciones OAuth**. Como parte del inicio de sesión, autorizas la aplicación OAuth en varias organizaciones, según las políticas de la organización con respecto a las aplicaciones OAuth. Puedes solicitar acceso y la organización puede aprobar la aplicación OAuth. Si necesitas volver a solicitar acceso o revocar cualquier acceso, puedes [controlar el estado de tu conexión con la aplicación OAuth](https://github.com/settings/connections/applications/903eccd8a9d2ff50288f).

- **Aunque parezca que tienes las credenciales de autorización correctas, la organización `github` ha habilitado restricciones de acceso de aplicaciones OAuth, lo que significa que el acceso a datos de terceros está limitado**. Esto se debe a que una organización restringe las aplicaciones OAuth. Algunos intentos de autorización para organizaciones pueden fallar si la organización no permite aplicaciones OAuth en absoluto. Esto puede afectar incluso el acceso a repositorios públicos en organizaciones que niegan el acceso a aplicaciones OAuth.

- **Recurso protegido por la aplicación SAML de la organización. Debes otorgar acceso a tu token OAuth a esta organización**. Es posible que estés iniciando sesión en una organización con control SAML, por ejemplo, Microsoft. Deberías:
  1. Cerrar sesión en Copilot Workspace.
  2. Pasar por la autenticación SAML en el navegador al mirar, por ejemplo, un repositorio de la organización.
  3. Luego iniciar sesión nuevamente en Copilot Workspace.

### Solución de Problemas con Repositorios Privados

- **No puedes acceder a un repositorio privado en tu propia cuenta**. Después de iniciar sesión, deberías poder acceder a tus repositorios privados personales a menos que hayas eliminado el acceso para la aplicación OAuth. Si tienes problemas, es posible que hayas llegado a Copilot Workspace a través de un enlace de uso compartido y solo hayas dado privilegios de repositorio público. Deberías cerrar sesión e iniciar sesión nuevamente, y esto debería restaurar el acceso. Si eso no funciona, deberías [verificar el estado de tu conexión con la aplicación OAuth](https://github.com/settings/connections/applications/903eccd8a9d2ff50288f).

## Advertencias de Ambigüedad

Si Copilot Workspace detecta que tu tarea es demasiado ambigua o poco clara (por ejemplo, no parece estar alineada con los objetivos/foco del repositorio), es posible que te advierta al respecto y te pida que aclares aún más la tarea antes de poder continuar. Esto se hace para evitar la especulación en la especificación y ayudarte a avanzar hacia el "pozo del éxito", ya que las etapas posteriores del flujo de trabajo funcionan mejor con suficiente detalle.

<img src="images/further-techniques/ambiguous-spec.png" width=600 alt="Especificación ambigua">

*Una advertencia de que una tarea es demasiado ambigua y que se necesita aclarar la intención*

### Solución de Problemas con Codespaces

- **No se pudo determinar el propietario facturable para un nuevo codespace, es posible que el repositorio no se pueda utilizar para un codespace**. La aplicación OAuth de CW no está instalada en la organización del propietario facturable.

Consulta la [Guía de Codespaces](codespaces-guide.md) para obtener más información sobre Codespaces y solucionar errores comunes.
