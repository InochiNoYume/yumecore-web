# YumeCore Web — Historial de trabajo

Este registro resume decisiones, implementaciones, correcciones, elementos retirados y puntos de continuidad del sitio público.

## 2026-10-12/13 — Invitación oficial y sincronización pública

### 22:15 (America/Santiago / UTC-03:00)

- Confirmada y mantenida como invitación canónica: `https://discord.gg/7QTeThJvrV`.
- `site-config.js` ahora expone el estado público `Invitación oficial, activa y permanente`.
- `support.html` muestra el estado de la invitación desde la configuración pública y usa la misma URL canónica.
- README actualizado para indicar que la invitación es oficial, activa y permanente.
- Se mantiene la regla de no sustituir la invitación sin confirmación explícita del propietario.

### CI

- **2026-10-12 22:15:06 America/Santiago / 2026-10-13 01:15:06 UTC** — commit `d529f10ee72d88fd614e0dfddb87d1ac08d5b2a7`.
- **Deploy YumeCore website #62 / run `38331227711` — SUCCESS**.
- Resultado: validación y publicación del sitio completadas correctamente.

Referencia: https://github.com/InochiNoYume/yumecore-web/actions/runs/38331227711

## Historial anterior

- El sitio público mantiene `site-config.js` como referencia de valores compartidos.
- La retención pública continúa alineada en 90 días.
- Las pull requests se validan sin publicar y los cambios aceptados en `main` pueden desplegarse.
- Los fallos históricos del validador de enlaces locales quedan documentados y no deben eliminarse del contexto.

## Decisiones que no deben revertirse accidentalmente

- No sustituir la invitación oficial por otra URL sin confirmación explícita del propietario.
- No introducir secretos o credenciales en páginas públicas.
- No publicar afirmaciones que contradigan el comportamiento real del bot.
- Mantener `site-config.js` como referencia de los valores públicos compartidos.
- Mantener la retención pública sincronizada con `TICKET_RETENTION_DAYS` del bot.

## Regla para continuar

Después de una modificación relevante, actualizar `PROJECT-HISTORY.md` y `PROJECT-STATE.md` con fecha, hora, qué cambió, resultado real de CI, referencia del run, fallos/correcciones y siguiente punto de trabajo.
