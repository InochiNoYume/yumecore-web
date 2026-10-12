# YumeCore Web — Historial de trabajo

Este registro resume decisiones, implementaciones, correcciones, elementos retirados y puntos de continuidad del sitio público. Su objetivo es que un desarrollador o una nueva sesión pueda retomar el trabajo sin reconstruir el contexto anterior.

## 2026-10-12 — Continuidad y publicación

### Implementado o alineado

- Sitio público de YumeCore en GitHub Pages.
- Invitación canónica y permanente de soporte: `https://discord.gg/7QTeThJvrV`.
- Invitación centralizada en `site-config.js` y consumida por la página de soporte.
- README, página de soporte y enlaces públicos alineados con la invitación canónica.
- Política pública de retención alineada con el bot: 90 días para tickets cerrados.
- Página de funciones.
- Página de tutorial.
- Página de soporte.
- Términos, privacidad, 404, sitemap y robots.
- Validación automática de HTML, `lang`, `title`, `h1`, `alt`, enlaces locales, anclas y archivos requeridos.

### Referencias públicas

```text
SUPPORT_SERVER_URL=https://discord.gg/7QTeThJvrV
TICKET_RETENTION_DAYS=90
SITE=https://inochinoyume.github.io/yumecore-web/
```

No se almacenan secretos, tokens ni credenciales en este repositorio.

## Historial de CI y errores relevantes

### Fallo del validador por `tutorial.html`

Una ejecución de CI falló cuando `features.html` enlazaba a `tutorial.html`, pero el archivo todavía no existía en el commit validado. El workflow hizo correctamente su trabajo al rechazar el enlace local roto.

La corrección consistió en añadir `tutorial.html` y conservar la comprobación de enlaces locales. Ese fallo queda registrado como antecedente y no como bloqueo actual si las ejecuciones posteriores están verdes.

### Publicación de Pages

El workflow separa validación y despliegue: las pull requests validan el sitio sin publicar y los eventos que no son pull request pueden desplegar a GitHub Pages. Esto evita publicar cambios no validados.

## Decisiones que no deben revertirse accidentalmente

- No sustituir la invitación oficial por otra URL sin confirmación explícita del propietario.
- No introducir secretos o credenciales en páginas públicas.
- No publicar afirmaciones que contradigan el comportamiento real del bot.
- Mantener `site-config.js` como referencia de los valores públicos compartidos.
- Revisar enlaces locales y sitemap cuando se añada una página.
- Mantener la retención pública sincronizada con `TICKET_RETENTION_DAYS` del bot.

## Lo que queda por verificar

1. CI verde después de cada cambio relevante.
2. Revisar todas las páginas para detectar URLs de soporte inconsistentes.
3. Revisar enlaces locales, anclas y sitemap después de nuevas páginas.
4. Revisar visualmente GitHub Pages tras el despliegue.
5. Mantener sincronizados invitación, retención y descripción de funciones con el bot.
6. Registrar aquí cualquier fallo de CI, su causa y su corrección.

## Regla para continuar

Antes de actuar, revisar `PROJECT-STATE.md`, este historial y el estado de CI. Después de una modificación relevante, actualizar ambos registros con qué cambió, por qué, qué se verificó, qué falló y cuál es el siguiente punto de trabajo.
