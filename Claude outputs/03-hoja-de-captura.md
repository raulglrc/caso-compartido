# T3 · Hoja de captura

Una fila por compromiso enviado. La completa el mago. El archivo para rellenar es `hoja-de-captura.csv`.

**Señal:** (a) % de compromisos con respuesta en menos de 24 h; (b) % de compromisos con respuesta `corrige`.
**Umbral:** (a) ≥70% **y** (b) ≥10%. **Mínimo para leer:** 30 compromisos; si no, `inconclusive`.

## Columnas

| Columna | Qué se anota |
|---|---|
| `lider_id` | ID de la encuesta del líder (R-xxx), el mismo de T1 |
| `reunion_n` | 1 o 2 (enlaza con la fila de T1) |
| `compromiso_n` | nº del compromiso dentro de la tarjeta |
| `responsable_rol` | rol del responsable (no su nombre) |
| `estuvo_en_la_reunion` | si / no / no se sabe |
| `canal` | correo / chat Teams |
| `hora_envio` | fecha y hora en que el líder envió el mensaje |
| `hora_respuesta` | fecha y hora de la respuesta, o vacío |
| `respuesta_en_24h` | si / no |
| `respuesta` | `confirma` · `corrige` · `otra` (respondió algo que no es ninguna de las dos) · `sin_respuesta` |
| `que_corrigio` | si `corrige`: `que` · `responsable` · `fecha` · `motivo` · `otro` (varios separados por `;`) |
| `texto_correccion` | la corrección tal como la escribió (sin datos personales) |
| `notas` | lo que el mago observe |

## Reglas de conteo (fijadas en el diseño; no se cambian)

- Cuenta como respuesta en menos de 24 h cualquier `confirma`, `corrige` u `otra` llegada antes de 24 h desde `hora_envio`.
- Solo `corrige` cuenta para la señal (b). Una respuesta `otra` que de hecho corrige algo se anota como `corrige`.

## Regla de decisión (del diseño)

continue si (a) ≥70% y (b) ≥10% · change si (a) entre 40% y 69% (probar otro canal) · change si (a) ≥70% y (b) <10% (repetir con tarjetas generadas por el modelo de T2) · discard si (a) <40%.
