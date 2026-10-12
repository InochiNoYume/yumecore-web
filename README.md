# YumeCore — Beyond Support

Sitio público de presentación de YumeCore, una herramienta independiente para organizar tickets y solicitudes en comunidades de Discord.

## Enlaces oficiales

- **Sitio web:** https://inochinoyume.github.io/yumecore-web/
- **Añadir el bot:** https://discord.com/oauth2/authorize?client_id=1549554629853843596
- **Servidor oficial de soporte:** https://discord.gg/7QTeThJvrV — invitación activa y permanente.
- **Página de soporte:** https://inochinoyume.github.io/yumecore-web/support.html
- **Términos de servicio:** https://inochinoyume.github.io/yumecore-web/terms.html
- **Política de privacidad:** https://inochinoyume.github.io/yumecore-web/privacy.html

> El enlace canónico de soporte es `https://discord.gg/7QTeThJvrV`. La invitación ha sido confirmada como activa y permanente por el propietario del proyecto. La misma URL se usa en `site-config.js`, la página de soporte y `SUPPORT_SERVER_URL` del bot.

## Política pública actual

- Retención de tickets cerrados: **90 días**.
- La política se refleja en `site-config.js` y debe mantenerse alineada con `TICKET_RETENTION_DAYS=90` del bot.
- Cuando el bot abandona una guild confirmada, sus datos y recursos asociados se eliminan de forma aislada. Una indisponibilidad temporal de Discord no se trata como expulsión.
- Las transcripciones privadas se almacenan en Supabase; las copias publicadas en Discord dependen de los permisos del canal configurado.

## Funciones destacadas

- Paneles de apertura con menú desplegable por categorías.
- Tickets privados con controles para Staff desde el propio canal.
- Reclamar/liberar, transferir, cambiar prioridad y estado, bloquear/desbloquear, participantes, notas e información del ticket.
- Cierre reservado al equipo de Staff; el solicitante no puede cerrar su propio ticket.
- Reapertura, archivo y papelera; las transcripciones se guardan en Supabase Storage privado y pueden publicarse como archivo en el canal configurado por cada servidor.
- Retención automática de tickets cerrados con la política actual de 90 días.
- Eliminación aislada de los datos de una guild cuando el bot es expulsado de ella; las guilds temporalmente no disponibles conservan sus datos.
- Resolución segura de paneles por UUID o nombre sin mezclar datos entre guilds.
- Configuración por servidor y tutorial interactivo por categorías mediante menús desplegables.
- Automatización, límites, anti-spam, backups y diagnóstico.
- Acceso interno separado para propietario y desarrolladores del bot, sin mezclarlos con el programa Beta Tester.

## Estructura

- `index.html`: página principal, funciones, guía conceptual y preguntas frecuentes.
- `support.html`: acceso oficial al servidor permanente de soporte.
- `features.html`: funciones principales del producto.
- `tutorial.html`: guía pública de configuración y puesta en marcha.
- `terms.html`: términos de servicio.
- `privacy.html`: política de privacidad.
- `404.html`: página de error personalizada.
- `site-config.js`: valores públicos compartidos, incluida la invitación canónica y la política pública de retención.
- `robots.txt` y `sitemap.xml`: directivas de rastreo y mapa de páginas.
- `123c7a37ea32e786c418e59e43da6a87.jpg`: imagen de marca usada en el sitio y como favicon.
- `.github/workflows/pages.yml`: validación de estructura, accesibilidad básica, enlaces locales y publicación mediante GitHub Pages.

## Publicación y CI

El sitio se publica mediante GitHub Pages y GitHub Actions. En **Settings → Pages**, la fuente de publicación debe estar configurada en **GitHub Actions**. Las pull requests se validan sin publicar; los cambios aceptados en `main` pueden desplegarse.

### Incidencias de CI conocidas

- Hubo un fallo histórico cuando `features.html` apuntaba a `tutorial.html` antes de que esa página existiera en el commit validado. El validador detectó correctamente el enlace local roto.
- La corrección fue añadir `tutorial.html` y conservar la comprobación automática de enlaces locales.
- Ese fallo se conserva como antecedente en `PROJECT-HISTORY.md`; no debe tratarse como bloqueo actual si las ejecuciones posteriores están verdes.

## Continuidad del proyecto

- [`PROJECT-STATE.md`](PROJECT-STATE.md): estado actual, verificaciones y próximo punto de continuación.
- [`PROJECT-HISTORY.md`](PROJECT-HISTORY.md): historial de implementaciones, cambios, errores, correcciones, elementos retirados y decisiones que no deben revertirse accidentalmente.

Antes de cambiar el sitio, revisa ambos archivos y el estado de CI. Si cambia el comportamiento público del bot, sincroniza este repositorio con él.

## Seguridad y privacidad

Este repositorio contiene los archivos públicos del sitio web. No añadas tokens, claves API, credenciales, código interno del bot ni detalles privados de infraestructura.

Los documentos legales describen el alcance general del servicio. Deben contrastarse con la implementación desplegada, los proveedores utilizados, los plazos reales de conservación y las obligaciones legales aplicables antes de considerarse asesoramiento o documentación legal definitiva.
