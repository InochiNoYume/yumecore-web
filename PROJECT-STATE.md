# YumeCore Web — Estado del proyecto

Última actualización: **2026-10-12 22:15 America/Santiago (UTC-03:00)**

Este archivo mantiene el contexto operativo del sitio público para que otro desarrollador o una nueva sesión pueda continuar sin reconstruir todo el historial.

## Estado actual

- Repositorio público: `InochiNoYume/yumecore-web`.
- Rama de publicación: `main`.
- Hosting: GitHub Pages.
- Workflow principal: `.github/workflows/pages.yml`.
- Sitio público: `https://inochinoyume.github.io/yumecore-web/`.
- Invitación oficial: `https://discord.gg/7QTeThJvrV`.
- Estado público de la invitación: **oficial, activa y permanente**.
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
- Estado público de la invitación centralizado en `site-config.js`.

## Invitación oficial

La URL canónica es:

`https://discord.gg/7QTeThJvrV`

Estado: **invitación oficial, activa y permanente**.

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

## Última verificación CI

- **Deploy YumeCore website #62**.
- Run: `38331227711`.
- Commit verificado: `d529f10ee72d88fd614e0dfddb87d1ac08d5b2a7`.
- Resultado: **SUCCESS**.
- Fecha/hora: **2026-10-12 22:15:06 America/Santiago**.

## Próximo punto de continuación

1. Mantener sincronizada la invitación entre bot y web.
2. Confirmar CI verde después de los commits de historial/estado posteriores a esta actualización.
3. Revisar visualmente GitHub Pages tras el despliegue más reciente.
4. Si se modifica el comportamiento del bot, actualizar este estado y `PROJECT-HISTORY.md`.

## Regla de continuidad

Este sitio es público. Solo debe contener información que pueda publicarse de forma segura. Las credenciales y detalles internos de infraestructura pertenecen al repositorio privado del bot y nunca deben copiarse aquí.
