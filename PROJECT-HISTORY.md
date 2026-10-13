# YumeCore Web — Historial de trabajo

Este registro resume decisiones, implementaciones, correcciones, elementos retirados y puntos de continuidad del sitio público.

## 2026-10-12/13 — Invitación oficial y sincronización pública

### Estado actual

- Invitación canónica: `https://discord.gg/7QTeThJvrV`.
- Estado público: **oficial, activa y permanente**.
- `site-config.js` expone la misma URL y el estado permanente.
- `support.html` muestra el mismo enlace y estado.
- La portada y el README utilizan la misma invitación.
- El bot `.env.example`, README y bienvenida validada usan exactamente la misma URL.
- No se sustituirá esta invitación por otra sin confirmación explícita del propietario.

### CI

- Deploy YumeCore website #62 / run `38331227711` — **SUCCESS**.
- La publicación correspondiente quedó validada correctamente.

Referencia: https://github.com/InochiNoYume/yumecore-web/actions/runs/38331227711

## Sincronización con el bot

El sitio queda alineado con el contrato público actual del bot: soporte oficial mediante la invitación permanente, sin introducir secretos ni valores privados. La retención pública continúa alineada en 90 días.

## Decisiones que no deben revertirse accidentalmente

- No sustituir la invitación oficial por otra URL sin confirmación explícita del propietario.
- No introducir secretos o credenciales en páginas públicas.
- No publicar afirmaciones que contradigan el comportamiento real del bot.
- Mantener `site-config.js` como referencia de los valores públicos compartidos.
- Mantener la retención pública sincronizada con `TICKET_RETENTION_DAYS` del bot.

## Regla para continuar

Después de una modificación relevante, actualizar `PROJECT-HISTORY.md` y `PROJECT-STATE.md` con fecha, hora, qué cambió, resultado real de CI, referencia del run, fallos/correcciones y siguiente punto de trabajo.


## 2026-10-13 — Auditoría de enlaces de la web pública

- Hallazgo: la portada no mostraba enlaces directos a `features.html` y `tutorial.html`, y las páginas secundarias no ofrecían una navegación consistente.
- Corrección: se añadió navegación cruzada Inicio, Funciones, Tutorial y Soporte, incluyendo la portada, el footer y la página de soporte.
- Prevención: el workflow ahora exige que las páginas públicas de funciones, tutorial, soporte y créditos estén presentes. El sitemap incorpora créditos.
- CI de `main` anterior a la auditoría: run `38344102428` — **SUCCESS**. CI de los cambios de esta rama pendiente de ejecutar mediante PR.
- No se fusionó ni se desplegó a producción.


## 2026-10-13 — Pulido premium y sincronización de la documentación pública

- PR #4 fusionada: navegación compartida, páginas públicas obligatorias en CI y sitemap actualizado.
- Añadidos `assets/yumecore-premium.css` y `assets/yumecore-effects.js` para una identidad premium/kawaii sin emojis decorativos, con acentos lavanda/rosa, animaciones suaves y partículas discretas. El efecto respeta `prefers-reduced-motion` y limita el trabajo en dispositivos móviles.
- PR #5 fusionada: el tutorial describe el flujo actual de tickets y la confirmación de cierre; se eliminaron pictogramas y flechas decorativas de la web pública.
- CI de la PR #5: run 38355548226 SUCCESS. Despliegue final de main: run 38355586854 SUCCESS.
