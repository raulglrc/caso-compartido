# T1 · Hoja de captura

Una fila por reunión. La completa el mago. El archivo para rellenar es `hoja-de-captura.csv`.

**Señal:** % de reuniones en que el líder envió la tarjeta **sin edición sustantiva** (columna `accion_lider` = `tal_cual` o `edicion_menor`).
**Umbral:** ≥60% (≥10 de 16). **Mínimo para leer:** 12 reuniones de al menos 6 líderes; si no, `inconclusive`.

## Columnas

| Columna | Qué se anota |
|---|---|
| `lider_id` | ID de la encuesta (R-xxx) |
| `perfil` | joaquin / beatriz / hernan (el que mejor encaje, según la llamada de arranque) |
| `usa_resumen_ia_hoy` | si / no |
| `procedencia` | `real` (miembro del segmento). Si alguien no lo es, `synthetic` y no cuenta para el umbral |
| `reunion_n` | 1 o 2 |
| `serie` | nombre de la serie |
| `fecha` | fecha de la reunión |
| `hora_fin_reunion` | hh:mm |
| `hora_envio_tarjeta` | hh:mm |
| `dentro_de_2h` | si / no |
| `n_decisiones_tarjeta` | nº de decisiones en la tarjeta |
| `n_campos_no_se_dijo` | nº de campos marcados "no se dijo" |
| `accion_lider` | `tal_cual` · `edicion_menor` · `edicion_sustantiva` · `descarto_y_escribio_el_suyo` · `no_envio_nada` |
| `campos_editados` | si hubo edición sustantiva: `decision_agregada`, `decision_quitada`, `decision_cambiada`, `responsable`, `fecha`, `motivo` (varios separados por `;`) |
| `donde_lo_envio` | correo / chat Teams / canal / Jira / otro |
| `minutos_declarados` | minutos que el líder dice que le llevó dejar el registro listo |
| `notas` | lo que el mago observe |

## Definiciones (fijadas en el diseño; no se cambian)

- **Edición sustantiva:** agregar, quitar o cambiar una decisión, un responsable, una fecha o un motivo. Completar un campo marcado "no se dijo" cuenta como edición sustantiva de ese campo.
- **Edición menor:** cambiar redacción, orden, formato o saludo, sin tocar el contenido de ninguna decisión.
- **Descartó y escribió el suyo:** lo que envió no parte de la tarjeta.
- **No envió nada:** a las 48 h, y tras un recordatorio, no llegó ningún registro.

## Regla de decisión (del diseño)

continue si ≥60% · change si 35–59% y las ediciones se concentran en un mismo campo · discard si <35%, o si `no_envio_nada` en ≥50% de las reuniones.
