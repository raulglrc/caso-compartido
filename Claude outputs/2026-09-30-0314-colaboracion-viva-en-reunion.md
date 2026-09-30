---
opportunity: colaboracion-viva-en-reunion
status: testing-several
chosen: recap-decisiones-confirmable, ritual-cierre
---

# Soluciones para: Colaboración visual en vivo durante la reunión, en cuentas tech grandes y distribuidas

## Qué dice hoy la evidencia

- **[value] de la oportunidad: `weakened`, no `contradicted`.** Se confirma que lo nativo no sostiene (43% probó Whiteboard y la dejó, `survey`; 4 de 5 entrevistados que la probaron, `real`), pero los tableros visuales solo aparecen en el 34% de las reuniones que salen de Teams; el 74% del trabajo en Docs/Jira/dashboards es sobre artefactos que ya existían (`survey`, product/insights/2026-09-30-0205-colaboracion-en-vivo-fuera-de-teams.md).
- **El dolor que se repite es cerrar y registrar la decisión**, no el lienzo: 10 de 10 entrevistas con un costo concreto (`real`, product/insights/2026-09-30-0211-colaboracion-en-vivo-entrevistas.md); 24% de reuniones sin registro (`survey`). El resumen de IA ya hace de acta y falla en los 6 de 6 que lo usan.
- **Lo nativo muere con la reunión**: 5 de 10 perdieron pizarra o notas al recrear la serie (`real`).
- **Acceso de externos**: real pero de otro segmento (21% de reuniones; "una vez al mes"). Dentro del segmento pesa quien se queda mirando o dicta (6 de 10, `real`; 46% de reuniones internas, `survey`).
- **Sigue abierto:** [viability] #4 (sin cruce contra renovaciones) y compliance en la UE (5 menciones, direccional).

**Decisión de encuadre (usuario, 2026-09-30):** se evalúa contra el problema como lo muestra la evidencia — **converger → decidir → registrar → retomar** — y no contra "colaboración visual". Queda pendiente reencuadrar el brief en dos ramas (decisión/registro vs. tablero visual) con `/frame-opportunity`.

## Línea base: qué hacen hoy

- El líder transcribe a mano después de la reunión (correo, Jira, acta), 10 a 60 minutos por reunión: 8 de 10, *"nadie más lo hace"* (`real`).
- El resumen de IA se reescribe (Javier, 30 min) o se corrige (Paula, 10 min) o se abandona (Martina) (`real`).
- Continuidad: un tablero de Miro por trimestre (Tomás, Javier) o capturas de pantalla pegadas en Confluence (Lucía) (`real`).
- Converger: reacciones o manos contadas a ojo; decide el líder cuando se acaba la hora (6 de 10) (`real`).
- Participación: se le dicta al que tiene el mouse (6 de 10) (`real`).

## Alternativas

### A1. Resumen de decisiones con IA, confirmado antes de cerrar (`recap-decisiones-confirmable`)
La IA separa lo decidido de lo conversado, con dueño, fecha y motivo; lo muestra en la reunión para confirmarlo antes de cortar, y lo envía adonde vive el trabajo (Jira, Planner, la serie). Ataca registrar y retomar. Personas: Camila Reyes Aguirre (primary), Agnieszka Wróbel (primary). Reemplaza la transcripción manual y la reescritura del recap.

### A2. Cierre explícito dentro de la reunión (`cierre-explicito`)
Momento de cierre nativo: propuesta visible, voto u objeción anónimos y bien contados (incluso para quien no entró al tablero), decisión registrada con quién la tomó. Absorbe la idea aparcada "votación o priorización en vivo". Ataca converger y decidir. Reemplaza reacciones a ojo y el "decido yo cuando se acaba la hora".

### A3. Pizarra nativa persistente, a la par de Miro (`whiteboard-persistente`)
Pizarra y notas ancladas a la serie o el canal, con link fijo; votar, agrupar, plantillas, rendimiento con más de 10 personas. Rama *construir* de "herramientas colaborativas integradas". Ataca continuidad y el tercio de reuniones que crea tableros. Reemplaza Miro y las capturas.

### A4. Integrar en vez de reconstruir (`artefacto-en-reunion`)
El artefacto externo (Jira, Power BI, Docs, Miro) como app de primera clase en la reunión, y cualquiera puede señalar o anotar sobre lo compartido sin licencia en la herramienta de origen. Rama *integrar* de "herramientas colaborativas integradas"; absorbe "documento editable en vivo". Ataca participación y el 74% de artefactos preexistentes. Reemplaza pegar links y dictar.

### A5. Ritual y plantilla con lo que ya existe — no es software (`ritual-cierre`)
Plantilla de agenda con sección "Decisiones (quién, qué, para cuándo)" en notas de Loop fijadas a la serie, regla de "últimos 5 minutos: leer las decisiones en voz alta", y campaña para dar a conocer notas de Loop y apps en reunión (31% y 40% no las conocían, `survey`). Absorbe "rediseño de descubribilidad", reorientado de Whiteboard a Loop y apps. Lo más chico que podría funcionar.

## Comparación

| Alternativa | Deseable | Factible | Viable | Creencia más riesgosa |
|---|---|---|---|---|
| A1 `recap-decisiones-confirmable` | strong — decisión perdida 10/10 y recap falla 6/6 (`real`, insights …0211); 14% ya lo usa como acta, 13/26 quejas; IA es la función nativa más adoptada, 36% (`survey`, insights …0205); pedido directo de Martina (`real`) | to check with tech — el recap existe; sin evidencia sobre precisión para separar decisiones con dueño/fecha ni envío a Jira/Planner | unknown — #4 abierta. `assumption`: se apoya en una función ya usada y podría diferenciar Max ("capacidades avanzadas de reuniones", overview) | Si el líder ve y confirma las decisiones antes de cerrar, deja de reescribir el registro después: en ≥60% de las reuniones se envía sin edición sustantiva |
| A2 `cierre-explicito` | mixed — el líder decide al acabarse el tiempo 6/10, votos sin confianza (`real`); pero "votar no decide" (Javier) y Paula/Ricardo sacan las decisiones de la reunión grande (`real`) | to check with tech | unknown | Un voto u objeción anónimo y bien contado hace aparecer el desacuerdo dentro de la reunión: cae la proporción de decisiones reabiertas después |
| A3 `whiteboard-persistente` | mixed — persistencia 5/10 (`real`), 43% dejó Whiteboard (`survey`); pero tableros solo en 34% de reuniones y 29% en intensidad alta (`survey`) | to check with tech — tiempo real en llamada es posible (Zoom, `secondary`, research …0532); paridad con Miro en 5 meses sin evidencia | unknown — solo creencia #2, sin verificar | Con persistencia + votar/agrupar, equipos que hoy crean tableros en Miro para la reunión eligen la pizarra nativa en ≥50% de esas sesiones |
| A4 `artefacto-en-reunion` | mixed — 74% de artefactos ya existían (`survey`); dictar 6/10, no poder señalar 4/10 (`real`); no ataca el registro ni sirve a cuentas con compliance | to check with tech — apps de Miro/Mural/FigJam en Teams existen (`secondary`); anotar sin licencia, sin evidencia | unknown | Señalar/anotar sin licencia baja la proporción de reuniones internas con alguien mirando desde afuera (hoy 46%) |
| A5 `ritual-cierre` | weak — no quita el trabajo de registrar, lo mueve al cierre; las notas de Loop también se pierden al recrear la serie (Paula, `real`) | strong — usa notas de Loop, plantillas y apps existentes (overview; Q10 de la encuesta) | weak (`assumption`) — no toca upgrade a Max; como mucho más uso de funciones ya pagadas | Los líderes sostienen un cierre manual durante ≥4 semanas sin que el producto lo haga por ellos |

Notas de lectura: la columna viable no discrimina hasta cruzar cuentas contra renovación (#4). A5 y A2 comparten la conducta de cierre explícito: A5 la prueba barato antes de construir A2. A1 es la única `strong` en deseable; sus citas son de la misma calidad que las demás, pero lo probado es el dolor, no el alivio — eso es su creencia más riesgosa.

## Decisión

Elegido por el usuario (2026-09-30): **A1 y A5 en paralelo** (`testing-several`), coincide con la recomendación.

- **Prueba de A1 — prototipo "de mago"** (una persona hace lo que haría la IA): con grabaciones reales de 6 a 8 Team Leads del grupo opt-in, se presentan las decisiones extraídas (dueño, fecha, motivo) para confirmar al cierre, y se mide cuánto se edita el registro después. Resuelve `[feature: recap-decisiones-confirmable] [value]`.
- **Prueba de A5 — piloto de 4 semanas** con 5 a 8 Team Leads, priorizando el grupo que no trabaja afuera (R-120, R-046, R-009…) y cuentas con compliance. Mide proporción de reuniones cerradas con decisiones registradas y cuántas se retoman en la reunión siguiente. Resuelve `[feature: ritual-cierre] [usability]` y, con eso, si vale la pena construir A2.
- **Dependencia para tech:** que lo decidido viva en la serie o el canal y no en la instancia de la reunión (pieza de A3), condición del "retomar" de A1.

**Qué cambiaría la decisión:** si en el prototipo los líderes siguen reescribiendo más de la mitad, o tech dice que la extracción no es viable en 5 meses → gana la vía A5/A2. Si el cruce de renovaciones muestra que cuentas con mucho Miro bajan de plan → sube A3.

## Propuesta de valor: A1 `recap-decisiones-confirmable`

Contra Camila Reyes Aguirre y Agnieszka Wróbel (primary):

- **Dolor que alivia:** la decisión se pierde entre la reunión y la ejecución, con costo de días a semanas (10/10, `real`); el recap de IA mezcla lo decidido con lo conversado y ya causó errores (Javier, Paula, `real`).
- **Ganancia:** al cortar la llamada, las decisiones ya están confirmadas por el grupo, con dueño, fecha y motivo, y están en el ticket o la serie sin que el líder las transcriba.
- **Reemplaza:** los 10 a 60 minutos de transcripción manual y la reescritura del recap; se cambia porque el registro deja de depender de que el líder "no se olvide" y de que alguien lea una transcripción de una hora.
- **Deliberadamente no:** no es un lienzo ni una pizarra; no vota ni facilita la discusión; no decide por el grupo (solo propone y se confirma); no reemplaza a Jira ni al tablero, escribe en ellos.

## Propuesta de valor: A5 `ritual-cierre`

Contra Camila Reyes Aguirre y Agnieszka Wróbel (primary), y el grupo que no trabaja afuera:

- **Dolor que alivia:** *"lo hago medio a mano y a veces se me va"* (Sofía, `real`); en el grupo sin herramienta externa, *"si no lo anoto yo no lo anota nadie"* (R-046, `survey`).
- **Ganancia:** la decisión se escribe y se lee en voz alta antes de cortar, y todos la escuchan, incluso quien no habló.
- **Reemplaza:** el acta escrita después y en solitario; se cambia porque cierra la reunión con acuerdo explícito, sin herramienta nueva.
- **Deliberadamente no:** no automatiza nada ni construye software; no resuelve la persistencia de las notas si la serie se recrea (se registra como riesgo del piloto).

## Creencias

- [opportunity: colaboracion-viva-en-reunion] [value] (#3 en product/overview.md, tal como está registrada, anotada `weakened` el 2026-09-30)
- [opportunity: colaboracion-viva-en-reunion] [viability] (#4 en product/overview.md, tal como está registrada)
- [feature: recap-decisiones-confirmable] [value] Cuando un Team Lead del segmento ve las decisiones extraídas (dueño, fecha, motivo) y las confirma antes de cerrar la reunión, deja de reescribir el registro después: en ≥60% de las reuniones el registro confirmado se envía sin edición sustantiva. — propuesta
- [feature: recap-decisiones-confirmable] [feasibility] Se pueden separar decisiones de conversación, con dueño y fecha, con precisión suficiente para que el líder no las reescriba, y enviarlas a Jira/Planner y a la serie, dentro del plazo de CollabCon y las restricciones de rendimiento y privacidad. — propuesta, to check with tech
- [feature: ritual-cierre] [usability] Los Team Leads del piloto sostienen un cierre explícito (decisiones escritas y leídas en voz alta en los últimos minutos) en ≥50% de sus reuniones de serie durante 4 semanas, sin que el producto lo haga por ellos. — propuesta

## Descartadas o aparcadas

- A2 `cierre-explicito` — parked: depende de la conducta que prueba A5; vuelve si el piloto de A5 muestra que los líderes sostienen el cierre explícito.
- A3 `whiteboard-persistente` — parked: dolor real pero secundario (34% de reuniones con tableros). Su pieza de persistencia en la serie pasa a dependencia de A1. Vuelve si el cruce de renovaciones vincula el uso de Miro con bajas de plan.
- A4 `artefacto-en-reunion` — parked: ataca la participación pero no el registro, y no sirve a cuentas con compliance. Vuelve si se abre la rama de "artefactos que viven afuera" al reencuadrar la oportunidad.
- Acceso de invitados externos sin cuenta — parked: problema de otro segmento (externos en el 21% de las reuniones, "una vez al mes"; demora de 5+ minutos concentrada ahí). Vuelve si la oportunidad se abre a consultoras y agencias.
