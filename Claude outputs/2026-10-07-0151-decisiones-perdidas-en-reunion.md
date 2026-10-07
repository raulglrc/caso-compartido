---
opportunity: decisiones-perdidas-en-reunion
solutions: product/solutions/2026-09-30-0339-decisiones-perdidas-en-reunion.md
also_covers: product/solutions/2026-09-30-0314-colaboracion-viva-en-reunion.md (A1 y A5, que cuelgan de esta rama tras el reencuadre)
status: designed
---

# Pruebas de solución para: Las decisiones de la reunión se pierden antes de llegar a la ejecución

## Por qué probar

Hay cuatro alternativas en prueba: A1 `recap-decisiones-confirmable` y A5 `ritual-cierre` (del archivo 0314), y B1 `acuse-de-compromiso` y B4 `escriba-rotativo` (del archivo 0339). Van en un solo archivo porque B1 corre dentro de la prueba de A1 y B4 es el segundo brazo de la de A5. **El dolor está demostrado** (10 de 10 entrevistas, 24% de reuniones sin registro); **que estas soluciones lo alivien, no**: nadie reaccionó todavía a ninguna de ellas. El único indicio sobre una solución parecida es parcial: las notas que toma otra persona en las reuniones de Paula "funcionan bien" (B4) y la guía de filtros de Diego P. se abandonó en la segunda semana (en contra de A5).

**Reclutamiento común:** grupo de la encuesta que aceptó una conversación (64 candidatos; 10 ya entrevistados), solo Team Leads del segmento que conducen al menos una reunión de serie por semana en la que se decide algo. T1/T3 y T4/T5 usan **grupos distintos** para que una prueba no contamine a la otra: 8 líderes para T1 y 12 a 16 para T4/T5. Cuentas con restricciones de compliance que no puedan compartir grabaciones van a T4/T5, no a T1.

## T1. recap-decisiones-confirmable: tarjeta de decisiones hecha a mano, enviada después de la reunión

- **Test status:** designed
- **Belief under test:** "8. [feature: recap-decisiones-confirmable] [value] Cuando un Team Lead del segmento ve las decisiones extraídas (dueño, fecha, motivo) y las confirma antes de cerrar la reunión, deja de reescribir el registro después: en ≥60% de las reuniones el registro confirmado se envía sin edición sustantiva."
- **Risk:** [value]
- **Test type:** wizard-of-oz
- **What we do:**
  1. El líder graba 2 reuniones de serie reales con decisiones (con el consentimiento de su equipo).
  2. Una persona del equipo de producto (el "mago") escucha la grabación y, **en menos de 2 horas**, le envía al líder una tarjeta con cada decisión: qué, responsable, fecha y motivo. Criterio del mago: es decisión solo lo que alguien acordó explícitamente; las ideas y propuestas sin cierre quedan fuera.
  3. El líder hace con la tarjeta lo que haría con su registro de siempre: la reenvía, la edita o la descarta y escribe el suyo. Se le pide que reenvíe con copia al mago.
  4. Se compara lo que el líder envió con la tarjeta.
  - Este primer paso prueba la tarjeta *después* de la reunión, no la confirmación *antes* de cerrar que dice la creencia; esa es el siguiente paso. La lógica: si el líder reescribe una tarjeta hecha con cuidado por una persona, A1 muere sin importar la IA.
- **With whom:** 8 Team Leads del segmento, del grupo opt-in; mezcla de los tres perfiles derivados (Joaquín Lemos, Beatriz Olmedo, Hernán Soto) y de quienes usan y no usan el resumen de IA hoy. Se esperan 16 reuniones.
- **Material needed:** (1) plantilla de tarjeta de decisiones: lista de decisiones con qué / responsable / fecha / motivo, sin resumen de la conversación; (2) guía del mago con el criterio de qué cuenta como decisión; (3) texto de invitación y consentimiento de grabación para el equipo del líder; (4) hoja de captura por reunión: hora de la reunión, hora de envío de la tarjeta, nº de decisiones, qué hizo el líder (reenvió tal cual / edición menor / edición sustantiva / descartó), qué campo cambió, minutos que el líder dice haber dedicado. Se deja fuera a propósito: cualquier interfaz, cualquier IA y cualquier resumen de lo conversado.
- **Material:** (lo agrega /build-solution-test)
- **Duration:** 2 semanas de campo (2 reuniones por líder) más 1 semana de reclutamiento.
- **Signal and threshold:** % de reuniones en que el líder envió la tarjeta **sin edición sustantiva**. Edición sustantiva = agregar, quitar o cambiar una decisión, un responsable, una fecha o un motivo; cambiar redacción no cuenta. **Umbral: ≥60% (≥10 de 16 reuniones).** Mínimo para leer el resultado: 12 reuniones de al menos 6 líderes; si no, `inconclusive`.
- **Decision rule:** continue si ≥60% · change si 35–59% y las ediciones se concentran en un mismo campo (rediseñar la tarjeta y repetir) · discard si <35%, o si en ≥50% de las reuniones el líder no envía nada.
- **Expected provenance:** real
- **Next step if it passes:** el mismo mago, dentro de la llamada, muestra la tarjeta en los últimos 5 minutos para confirmarla antes de cerrar — la creencia #8 completa. Ese paso se diseña aparte.

## T2. recap-decisiones-confirmable: extracción automática contra las tarjetas confirmadas

- **Test status:** designed
- **Belief under test:** "9. [feature: recap-decisiones-confirmable] [feasibility] Se pueden separar decisiones de conversación, con dueño y fecha, con precisión suficiente para que el líder no las reescriba, y enviarlas a Jira/Planner y a la serie, dentro del plazo de CollabCon y las restricciones de rendimiento y privacidad. — to check with tech"
- **Risk:** [feasibility] — owner: tech
- **Test type:** technical-test
- **What we do:** tech corre el modelo de extracción sobre las transcripciones de las reuniones de T1 y compara su salida contra la **clave de respuestas**: las tarjetas tal como las dejó el líder después de editarlas en T1. Solo cubre la extracción; el envío a Jira/Planner y la serie queda fuera de este paso.
- **With whom:** sin participantes; datos de las ≥12 reuniones de T1 cuyos líderes autorizaron el uso de la transcripción.
- **Material needed:** transcripciones de T1; clave de respuestas (tarjetas finales de T1); hoja de comparación por decisión (en la clave / en la salida / responsable correcto / fecha correcta). Se deja fuera: interfaz, integración con Jira.
- **Material:** (lo agrega /build-solution-test)
- **Duration:** 1 semana después de cerrar T1.
- **Signal and threshold:** propuestos por producto, **tech los confirma o ajusta antes de correr y el ajuste queda escrito aquí**: precisión de decisiones (lo que el modelo marca como decisión y sí lo es) **≥90%** — el error que ya causó daño es marcar ideas como decisiones (Paula); exhaustividad **≥80%**; responsable correcto en **≥85%** de las decisiones encontradas.
- **Decision rule:** continue si cumple los tres · change si la precisión cumple pero la exhaustividad no (el paso de confirmación puede cubrir lo que falta; rediseñar la confirmación) · discard si la precisión queda por debajo del 75%.
- **Expected provenance:** real
- **Next step if it passes:** prueba técnica de rendimiento y privacidad en el contexto de la reunión, y del envío a Jira/Planner (diseñada con tech).

## T3. acuse-de-compromiso: cada responsable confirma o corrige su compromiso

- **Test status:** designed
- **Belief under test:** "15. [feature: acuse-de-compromiso] [value] Cuando cada responsable recibe su compromiso (qué, para cuándo, por qué) después de la reunión, ≥70% lo confirma o corrige en menos de 24 horas y al menos 1 de cada 10 corrige algo que el registro tenía mal o ambiguo."
- **Risk:** [value]
- **Test type:** wizard-of-oz
- **What we do:** dentro de T1, después de que el líder reenvía la tarjeta, cada responsable nombrado recibe un mensaje individual con **solo su compromiso** (qué, para cuándo, por qué) y dos respuestas posibles: "confirmo" o "corrijo: …". Lo envía el líder con un texto preparado, desde su cuenta, para que llegue como llegaría en el producto.
- **With whom:** los responsables nombrados en las tarjetas de T1 (se esperan 40 a 50 compromisos), con autorización del líder.
- **Material needed:** plantilla de mensaje individual por compromiso, con las dos respuestas; hoja de captura por compromiso: hora de envío, hora de respuesta, confirma / corrige / sin respuesta, qué corrigió. Se deja fuera: recordatorios y seguimiento del cumplimiento.
- **Material:** (lo agrega /build-solution-test)
- **Duration:** la misma ventana de T1; cada compromiso se mide a las 24 h.
- **Signal and threshold:** **≥70%** de los compromisos con respuesta en menos de 24 h **y** correcciones en **≥10%** de los compromisos. Mínimo para leer: 30 compromisos; si no, `inconclusive`.
- **Decision rule:** continue si cumple las dos · change si responde entre 40% y 69% (probar otro canal: tarea de Planner o mensaje en Teams en vez de correo) · change si responde ≥70% pero corrige <10% (las tarjetas de T1 las hizo una persona con cuidado; repetir cuando la tarjeta salga de la IA en T2) · discard si responde <40%.
- **Expected provenance:** real
- **Next step if it passes:** repetirlo con tarjetas generadas por el modelo de T2, donde se esperan más errores que atrapar.

## T4. ritual-cierre: plantilla y regla de cierre, 2 semanas

- **Test status:** designed
- **Belief under test:** "10. [feature: ritual-cierre] [usability] Los Team Leads del piloto sostienen un cierre explícito (decisiones escritas y leídas en voz alta en los últimos minutos) en ≥50% de sus reuniones de serie durante 4 semanas, sin que el producto lo haga por ellos."
- **Risk:** [usability]
- **Test type:** concierge
- **What we do:** el líder usa en sus reuniones de serie una plantilla de notas con la sección "Decisiones (qué, quién, para cuándo, por qué)", fijada a la serie, y la regla "en los últimos 5 minutos se escriben y se leen en voz alta". El equipo de producto hace una sesión de arranque de 20 minutos y no vuelve a intervenir: sin recordatorios.
- **With whom:** brazo A, 6 a 8 Team Leads del grupo opt-in, distintos de los de T1; asignación alternada con T5, equilibrando perfiles (Joaquín / Beatriz / Hernán) y priorizando quienes no trabajan afuera y cuentas con compliance (R-120, R-046, R-009 y siguientes).
- **Material needed:** plantilla de notas de la reunión con la sección de decisiones; tarjeta de una página con la regla; guion de la sesión de arranque; hoja de captura por reunión: fecha, ¿se completó la sección antes del final? (marca de tiempo de las notas), ¿se leyó en voz alta? (registro del líder), nº de decisiones. Se deja fuera: recordatorios, IA, integración con Jira.
- **Material:** (lo agrega /build-solution-test)
- **Duration:** 2 semanas de uso más 1 semana de arranque.
- **Signal and threshold:** % de reuniones de serie de la **semana 2** con cierre hecho (sección completada antes del final y leída en voz alta). **Umbral: ≥50%.** Se mide la semana 2 porque el riesgo es el abandono, y la evidencia muestra que llega ahí. Mínimo: 10 reuniones en la semana 2; si no, `inconclusive`.
- **Decision rule:** continue si ≥50% en la semana 2 · change si 25–49% (ver qué lo frenó: tiempo, olvido, el líder no puede escribir y moderar a la vez; ajustar y repetir) · discard si <25%.
- **Expected provenance:** real
- **Next step if it passes:** extender a 4 semanas con los mismos líderes; recién ahí se resuelve la creencia #10 completa.

## T5. escriba-rotativo: un participante registra las decisiones, 2 semanas

- **Test status:** designed
- **Belief under test:** "16. [feature: escriba-rotativo] [value] Cuando un participante que no es el líder registra las decisiones en vivo en las notas de la serie, el líder no reescribe ese registro en ≥60% de las reuniones durante 4 semanas."
- **Risk:** [value]
- **Test type:** concierge
- **What we do:** igual que T4, con la misma plantilla, pero el líder designa en cada reunión a un escriba que no es él (rota entre participantes) y que completa la sección de decisiones en vivo. El líder no tiene que leerla en voz alta. Después de la reunión, el líder hace con ese registro lo que haría siempre.
- **With whom:** brazo B, 6 a 8 Team Leads, asignados en alternancia con T4.
- **Material needed:** la misma plantilla de T4; tarjeta de una página para el escriba (qué cuenta como decisión); hoja de captura por reunión: ¿hubo escriba?, quién, nº de decisiones, qué hizo el líder con el registro en las 48 h siguientes (lo usó tal cual / edición menor / edición sustantiva / lo reescribió). Edición sustantiva con la misma definición que T1.
- **Material:** (lo agrega /build-solution-test)
- **Duration:** 2 semanas de uso más 1 semana de arranque (en paralelo con T4).
- **Signal and threshold:** % de reuniones con escriba en las que el líder **no** hizo edición sustantiva ni reescribió. **Umbral: ≥60%.** Si hubo escriba en menos del 50% de las reuniones, el resultado es `inconclusive` (no se probó el mecanismo).
- **Decision rule:** continue si ≥60% · change si 35–59% (ver qué corrige el líder; entrenar al escriba o cambiar la plantilla) · discard si <35%.
- **Expected provenance:** real
- **Next step if it passes:** extender a 4 semanas; la comparación con T4 es descriptiva (6 a 8 por brazo no da para más) y sirve para elegir entre cierre del líder y escriba, o combinarlos.

## Orden y calendario

| Semana | T1 / T3 | T2 | T4 / T5 |
|---|---|---|---|
| 1 | reclutamiento y consentimientos | — | reclutamiento y sesión de arranque |
| 2–3 | campo (2 reuniones por líder) | — | campo |
| 4 | — | tech corre la prueba | análisis |
| 5 | análisis conjunto con /analyze-solution-tests | | |

## Resultados

(Los agrega /analyze-solution-tests.)

## Decisión

(La agrega /analyze-solution-tests.)
