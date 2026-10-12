# YumeCore — Beyond Support

Sitio público de presentación de YumeCore, una herramienta independiente para organizar tickets y solicitudes en comunidades de Discord.

## Enlaces oficiales

- **Sitio web:** https://inochinoyume.github.io/yumecore-web/
- **Añadir el bot:** https://discord.com/oauth2/authorize?client_id=1549554629853843596
- **Servidor oficial de soporte:** https://discord.gg/7QTeThJvrV — invitación permanente.
- **Página de soporte:** https://inochinoyume.github.io/yumecore-web/support.html
- **Términos de servicio:** https://inochinoyume.github.io/yumecore-web/terms.html
- **Política de privacidad:** https://inochinoyume.github.io/yumecore-web/privacy.html

## Funciones destacadas

- Paneles de apertura con menú desplegable por categorías.
- Tickets privados con controles para Staff desde el propio canal.
- Reclamar/liberar, transferir, cambiar prioridad y estado, bloquear/desbloquear, participantes, notas e información del ticket.
- Cierre reservado al equipo de Staff; el solicitante no puede cerrar su propio ticket.
- Reapertura, archivo y papelera; las transcripciones se guardan en Supabase Storage privado y pueden publicarse como archivo en el canal configurado por cada servidor.
- Configuración por servidor y tutorial interactivo por categorías.
- Automatización, límites, anti-spam, backups y diagnóstico.
- Acceso interno separado para propietario y desarrolladores del bot, sin mezclarlos con el programa Beta Tester.

## Estructura

- `index.html`: página principal, funciones, guía conceptual y preguntas frecuentes.
- `support.html`: acceso oficial al servidor permanente de soporte.
- `terms.html`: términos de servicio.
- `privacy.html`: política de privacidad.
- `404.html`: página de error personalizada.
- `robots.txt` y `sitemap.xml`: directivas de rastreo y mapa de páginas.
- `123c7a37ea32e786c418e59e43da6a87.jpg`: imagen de marca usada en el sitio y como favicon.
- `.github/workflows/pages.yml`: validación de estructura, accesibilidad básica, enlaces locales y publicación mediante GitHub Pages.

## Publicación

El sitio se publica mediante GitHub Pages y GitHub Actions. En **Settings → Pages**, la fuente de publicación debe estar configurada en **GitHub Actions**. Las actualizaciones se validan antes de publicar.

## Seguridad y privacidad

Este repositorio contiene los archivos públicos del sitio web. No añadas tokens, claves API, credenciales, código interno del bot ni detalles privados de infraestructura.

Los documentos legales describen el alcance general del servicio. Deben contrastarse con la implementación desplegada, los proveedores utilizados, los plazos reales de conservación y las obligaciones legales aplicables antes de considerarse asesoramiento o documentación legal definitiva.
