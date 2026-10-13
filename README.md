# YumeCore — Beyond Support

Sitio público de presentación de YumeCore, una herramienta independiente para organizar tickets y solicitudes en comunidades de Discord.

## Enlaces oficiales

- **Sitio web:** https://inochinoyume.github.io/yumecore-web/
- **Añadir el bot:** https://discord.com/oauth2/authorize?client_id=1549554629853843596
- **Servidor oficial de soporte:** https://discord.gg/7QTeThJvrV — invitación activa y permanente.
- **Página de soporte:** https://inochinoyume.github.io/yumecore-web/support.html
- **Términos de servicio:** https://inochinoyume.github.io/yumecore-web/terms.html
- **Política de privacidad:** https://inochinoyume.github.io/yumecore-web/privacy.html

> El enlace canónico de soporte es `https://discord.gg/7QTeThJvrV`. La misma URL debe mantenerse en `site-config.js`, la página de soporte y `SUPPORT_SERVER_URL` del bot.

## Configuración global y por guild

YumeCore separa la configuración del proyecto de la configuración propia de cada comunidad.

### Global — gestionado por el propietario de YumeCore

Los valores globales del bot se mantienen en el entorno privado de la aplicación. Aquí entran los textos globales de bienvenida, términos, privacidad, créditos y tutorial, además de credenciales y otros valores operativos. Estos textos no los modifica el owner de una guild.

### Por guild — gestionado desde Discord

Cada owner/administrador de una guild configura desde Discord sus paneles, categorías, formularios, preguntas, mensajes de tickets, mensajes de apertura/cierre, mensajes operativos enviados durante la atención de tickets, permisos, roles, canales, prioridades, automatización, apariencia y demás opciones de su comunidad.

Esta configuración se almacena de forma aislada por `guild_id`. Los mensajes específicos de tickets y de Staff no se guardan en el `.env` global.

## Política pública actual

- Retención de registros de tickets eliminados: **90 días**.
- La política se refleja en `site-config.js` y debe mantenerse alineada con `TICKET_RETENTION_DAYS=90` del bot.
- Cuando el bot abandona una guild confirmada, sus datos y recursos asociados se eliminan de forma aislada. Una indisponibilidad temporal de Discord no se trata como expulsión.
- Las transcripciones privadas se almacenan en Supabase; las copias publicadas en Discord dependen de los permisos del canal configurado.

## Funciones destacadas

- Paneles y categorías completamente definidos por cada servidor.
- Formularios configurados por cada guild.
- Mensajes de apertura, cierre, Staff y demás contenido operativo configurables por guild desde Discord.
- Bienvenida, términos, privacidad, créditos y tutorial globales administrados por el propietario del bot.
- Menús desplegables para las acciones persistentes del ticket.
- Reclamar/liberar, transferir, prioridad, estado, participantes, bloqueo, notas, información e historial.
- Cierre que genera el transcript y elimina inmediatamente el canal. No hay archivado ni reapertura.
- Encuesta 1–5 mediante menú desplegable privado enviado al solicitante.
- Retención automática según la política actual de 90 días.
- Eliminación aislada de los datos de una guild cuando el bot es expulsado; las guilds temporalmente no disponibles conservan sus datos.
- Developers/gestores por guild administrados desde Discord, sin IDs de configuración en `.env`.
- Programa Beta con diagnóstico, pruebas de configuración y feedback; avatar y banner globales reservados al propietario del bot.
- Automatización, anti-spam, backups, diagnóstico y auditoría.

## Estructura

- `index.html`: página principal y presentación.
- `support.html`: acceso al servidor permanente de soporte.
- `features.html`: funciones actuales del producto.
- `tutorial.html`: guía pública de configuración y puesta en marcha.
- `terms.html`: términos de servicio.
- `privacy.html`: política de privacidad.
- `site-config.js`: valores públicos compartidos, incluida la invitación canónica y la política de retención.
- `.github/workflows/pages.yml`: validación y publicación mediante GitHub Pages.

## Publicación y CI

El sitio se publica mediante GitHub Pages y GitHub Actions. Las pull requests se validan sin publicar; los cambios aceptados en `main` pueden desplegarse.

## Continuidad del proyecto

- `PROJECT-STATE.md`: estado actual y verificaciones.
- `PROJECT-HISTORY.md`: historial de implementaciones y decisiones de continuidad.

Antes de cambiar el sitio, revisa ambos archivos y el estado de CI. Si cambia el comportamiento público del bot, sincroniza este repositorio con él.

## Seguridad y privacidad

Este repositorio contiene los archivos públicos del sitio web. No añadas tokens, claves API, credenciales, código interno del bot ni detalles privados de infraestructura.
