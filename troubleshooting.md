## Solución de Problemas

### Introducción

¡Bienvenido a la guía de solución de problemas de Copilot Workspace! En esta sección, te proporcionaremos consejos útiles y soluciones a problemas comunes que puedes encontrar al trabajar con organizaciones y repositorios privados en Copilot Workspace. Nuestro objetivo es asegurarnos de que tengas una experiencia fluida y productiva. ¡Vamos a sumergirnos!

### Troubleshooting access

If you are seeing an "Access Denied" error when trying Copilot Workspace for the first time, here are a few steps that may help:

- Make sure you have an active, paid copilot license. Trial licenses only allow access once the subscription is upgraded to a paid plan.
- Ensure there are no [trade restrictions](https://docs.github.com/en/site-policy/other-site-policies/github-and-trade-controls) on your account.
- Verify that any organization with Copilot enabled has both the **Copilot Preview Features** setting and the **Copilot Extensions setting** turned ON. If necessary, reach out to your organization’s administrator for assistance. For more details on configuring organization settings for Copilot, please refer to the [documentation](https://docs.github.com/en/copilot/managing-copilot/managing-github-copilot-in-your-organization/managing-policies-for-copilot-in-your-organization).
- For Enterprise users, enable the Copilot Workspace policy through your enterprise account (note this means accepting the [GitHub Next Terms and Conditions](https://github.com/githubnext/githubnext/blob/main/TERMS_AND_CONDITIONS.md))

### Troubleshooting Organizations

Cuando trabajas con organizaciones en Copilot Workspace, es posible que encuentres algunos problemas comunes. Aquí tienes algunos consejos de solución de problemas para ayudarte a resolverlos:

- **Estás accediendo a una organización que debe aprobar las aplicaciones OAuth**. Como parte del inicio de sesión, autorizas la aplicación OAuth en varias organizaciones, según las políticas de la organización con respecto a las aplicaciones OAuth. Puedes solicitar acceso y la organización puede aprobar la aplicación OAuth. Si necesitas volver a solicitar acceso o revocar cualquier acceso, puedes [controlar el estado de tu conexión con la aplicación OAuth](https://github.com/settings/connections/applications/903eccd8a9d2ff50288f).

- **Aunque parezca que tienes las credenciales de autorización correctas, la organización `github` ha habilitado restricciones de acceso de aplicaciones OAuth, lo que significa que el acceso a datos de terceros está limitado**. Esto se debe a que una organización restringe las aplicaciones OAuth. Algunos intentos de autorización para organizaciones pueden fallar si la organización no permite aplicaciones OAuth en absoluto. Esto puede afectar incluso el acceso a repositorios públicos en organizaciones que niegan el acceso a aplicaciones OAuth.

- **Resource protected by organization SAML enforcement. You must grant your OAuth token access to this organization**.You may be logging in to an organization with SAML control, e.g. Microsoft. They should
  1. Log out of Copilot Workspace.
  2. Go through SAML auth in the browser by looking at, say, a repository of the organization
  3. Then log back into Copilot Workspace.
- **Other known limitations to working within organizations:**
  1. The enterprise (or org) must opt-in to Copilot feature previews. [Learn how to enable feature previews in GitHub.com](https://docs.github.com/en/get-started/using-github/exploring-early-access-releases-with-feature-preview).
  2. The enterprise (or org) has set the Copilot Extension policy to Enabled. This can be done under your org / enterprise settings under Copilot > Copilot Policies.
    **Note:** Due to limitations with Copilot Licensing, all organizations of which you are a member must enable the Copilot Extension policy and opt-in for Copilot feature previews. If any organization of which you are a member disables these settings, you will not be able to access Copilot Workspace.
  4. Developers within the enterprise (or org) must have paid Copilot licenses.


### Solución de Problemas con Repositorios Privados

- **No puedes acceder a un repositorio privado en tu propia cuenta**. Después de iniciar sesión, deberías poder acceder a tus repositorios privados personales a menos que hayas eliminado el acceso para la aplicación OAuth. Si tienes problemas, es posible que hayas llegado a Copilot Workspace a través de un enlace de uso compartido y solo hayas dado privilegios de repositorio público. Deberías cerrar sesión e iniciar sesión nuevamente, y esto debería restaurar el acceso. Si eso no funciona, deberías [verificar el estado de tu conexión con la aplicación OAuth](https://github.com/settings/connections/applications/903eccd8a9d2ff50288f).

## Advertencias de Ambigüedad

Si Copilot Workspace detecta que tu tarea es demasiado ambigua o poco clara (por ejemplo, no parece estar alineada con los objetivos/foco del repositorio), es posible que te advierta al respecto y te pida que aclares aún más la tarea antes de poder continuar. Esto se hace para evitar la especulación en la especificación y ayudarte a avanzar hacia el "pozo del éxito", ya que las etapas posteriores del flujo de trabajo funcionan mejor con suficiente detalle.

<img src="images/further-techniques/ambiguous-spec.png" width=600 alt="Especificación ambigua">

*Una advertencia de que una tarea es demasiado ambigua y que se necesita aclarar la intención*

### Solución de Problemas con Codespaces

- **No se pudo determinar el propietario facturable para un nuevo codespace, es posible que el repositorio no se pueda utilizar para un codespace**. La aplicación OAuth de CW no está instalada en la organización del propietario facturable.

Consulta la [Guía de Codespaces](codespaces-guide.md) para obtener más información sobre Codespaces y solucionar errores comunes.
