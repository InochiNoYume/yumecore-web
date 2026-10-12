# YumeCore Web — Estado del proyecto

Última actualización: 2026-10-12

Este archivo mantiene el contexto operativo del sitio público para que otro desarrollador o una nueva sesión pueda continuar sin reconstruir todo el historial.

## Registro de continuidad

- `PROJECT-HISTORY.md` contiene el historial de implementaciones, cambios, errores, correcciones, elementos retirados y decisiones de continuidad.
- Antes de continuar una tarea, revisar este archivo, `PROJECT-HISTORY.md` y el estado de CI.
- Después de una modificación relevante, actualizar el estado y el historial con el resultado real de la verificación.

## Estado actual

- Repositorio público: `InochiNoYume/yumecore-web`.
- Rama de publicación: `main`.
- Hosting: GitHub Pages.
- Workflow principal: `.github/workflows/pages.yml`.
- Sitio público: `https://inochinoyume.github.io/yumecore-web/`.
- Invitación oficial: `https://discord.gg/7QTeThJvrV`.
- Política pública de retención: 90 días.

## Implementado

- Landing pública de YumeCore.
- Página de funciones.
- Página de tutorial.
- Página dedicada al soporte oficial.
- Términos y política de privacidad alineados con el comportamiento actual del bot.
- Página 404 personalizada.
- Sitemap y robots.
- Navegación móvil.
- Validación automática de HTML, títulos, `h1`, `alt`, enlaces locales, anclas y recursos requeridos.
- Publicación automática mediante GitHub Pages.
- Configuración pública compartida en `site-config.js`.

## Invitación oficial

La URL canónica es:

`https://discord.gg/7QTeThJvrV`

Debe permanecer igual en:

- `site-config.js`.
- `support.html`.
- README.
- enlaces públicos relevantes.
- `SUPPORT_SERVER_URL` del bot.
- mensaje de bienvenida del bot.

No sustituirla por una invitación nueva salvo que el propietario proporcione y confirme otra invitación oficial.

## Política de retención

La política pública actual es de 90 días para tickets cerrados. El valor público se mantiene en `site-config.js` y debe coincidir con `TICKET_RETENTION_DAYS=90` del bot.

## Errores encontrados y resolución

### CI de la web: enlace a tutorial inexistente

El workflow falló en el commit que añadió `features.html` porque el validador detectó:

`features.html: enlace/recurso local roto: tutorial.html`

El problema era de orden de publicación: `features.html` ya enlazaba al tutorial, pero `tutorial.html` todavía no existía en ese commit.

Después se añadió `tutorial.html` y se mantuvo la comprobación de enlaces locales. El fallo histórico se conserva como contexto en `PROJECT-HISTORY.md`; el estado actual debe comprobarse en la ejecución más reciente de Actions.

## Cambios recientes

- Se alinearon las páginas públicas con la política de retención de 90 días.
- Se publicó la invitación permanente oficial en la página de soporte.
- Se hizo que `support.html` tome la URL canónica desde `site-config.js`, manteniendo un fallback visible en HTML.
- README actualizado con enlaces oficiales, política actual y continuidad del proyecto.
- Se añadió `PROJECT-HISTORY.md` para conservar el historial de trabajo y facilitar la continuidad.

## Elementos retirados o que no deben volver

- Invitaciones de soporte no verificadas o antiguas.
- Información privada del bot, secretos, tokens o credenciales.
- Afirmaciones públicas que contradigan la retención o el aislamiento real del backend.
- Enlaces locales a páginas que no existan en el mismo commit.

## Próximo punto de continuación

1. Confirmar CI verde después de los últimos cambios.
2. Revisar todas las páginas buscando URLs de soporte inconsistentes.
3. Revisar enlaces locales y sitemap después de cualquier nueva página.
4. Mantener sincronizados invitación, retención y descripción de funciones con el bot.
5. Hacer una revisión visual final en GitHub Pages después del despliegue.
6. Si se modifica el bot, actualizar este estado cuando cambie el comportamiento público.

## Regla de continuidad

Este sitio es público. Solo debe contener información que pueda publicarse de forma segura. Las credenciales y detalles internos de infraestructura pertenecen al repositorio privado del bot y nunca deben copiarse aquí.
