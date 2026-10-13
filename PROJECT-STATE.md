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


## Auditoría de navegación y enlaces — 2026-10-13

### Hallazgos

- Las páginas `features.html`, `tutorial.html` y `support.html` sí existen en el repositorio público, pero la portada no enlazaba directamente a la página completa de funciones ni al tutorial desde su navegación principal.
- Las páginas de funciones y tutorial solo tenían la marca/enlace de regreso al inicio en el encabezado, sin navegación compartida entre las páginas.
- La lista de archivos requeridos del workflow no exigía `features.html`, `tutorial.html`, `support.html` ni `credits.html`; por tanto, una página principal secundaria podía desaparecer sin fallar ese control específico.
- El sitemap incluía funciones, tutorial y soporte, pero omitía créditos.

### Cambios en la rama `fix/site-navigation-audit`

- Añadidos enlaces directos a Funciones y Tutorial en la navegación y el pie de la portada.
- Añadida navegación coherente Inicio / Funciones / Tutorial / Soporte a las páginas de funciones y tutorial.
- Añadidos enlaces cruzados a Funciones y Tutorial en Soporte.
- Ampliada la lista obligatoria del CI para todas las páginas públicas clave y `site-config.js`.
- Añadida la página de créditos al sitemap.

### Verificación

- La última ejecución de la rama `main` antes de estos cambios fue Deploy YumeCore website #64, run `38344102428`, **SUCCESS**.
- Workflow de la PR #4: run `38350032168` — **SUCCESS** en el commit `46a7a0b4dc37078a52e149475fe1c9c9e5118694`. La validación estática pasó; el job de deploy fue omitido correctamente al ser una PR.
- No se ha publicado la rama de auditoría a GitHub Pages ni se ha modificado `main`; la PR #4 sigue abierta en borrador.
- La comprobación directa de las páginas publicadas no estuvo disponible mediante el lector web en esta sesión; los hallazgos de navegación se basan en el HTML fuente y el workflow del repositorio.
