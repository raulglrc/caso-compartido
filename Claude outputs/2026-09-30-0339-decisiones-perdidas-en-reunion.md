---
opportunity: decisiones-perdidas-en-reunion
status: testing-several
chosen: acuse-de-compromiso, escriba-rotativo
---

# Soluciones para: Las decisiones de la reunión se pierden antes de llegar a la ejecución

Segunda exploración de esta oportunidad. La primera ([2026-09-30-0314-colaboracion-viva-en-reunion.md](2026-09-30-0314-colaboracion-viva-en-reunion.md), hecha sobre el brief padre antes del reencuadre) eligió A1 `recap-decisiones-confirmable` y A5 `ritual-cierre`, que siguen en prueba y aquí son la referencia, no se reevalúan. Esta exploración abre mecanismos que el primer set no cubría.

## Qué dice hoy la evidencia

- **[value] #11** sin anotación, sostenida por la evidencia: decisión perdida con costo concreto en 10 de 10 entrevistas (`real`, product/insights/2026-09-30-0211-colaboracion-en-vivo-entrevistas.md); 24% de reuniones sin registro (`survey`, product/insights/2026-09-30-0205-colaboracion-en-vivo-fuera-de-teams.md); 8 de 10 transcriben a mano, 10 a 60 minutos.
- **[viability] #12** abierta: no se hizo el cruce contra renovaciones.
- **Nada nuevo desde la primera exploración** salvo las personas derivadas: Joaquín Lemos (primary), Beatriz Olmedo (primary) y Hernán Soto (secondary).
- A1 y A5 elegidas y sin resultados todavía.

## Línea base: qué hacen hoy

- El líder transcribe a mano después (correo, Jira, acta), 10 a 60 minutos: 8 de 10 (`real`).
- El resumen de IA se reescribe o se abandona (Javier, Paula, Martina, `real`).
- Cuando no hay acuerdo, decide el líder al acabarse la hora: 6 de 10 (`real`).
- Nadie verifica que el responsable entendió lo mismo: el correo sale y se supone leído (Andrés, Diego P., `real`).

## Alternativas

### Referencia (en prueba, no reevaluadas)
- A1 `recap-decisiones-confirmable` — la IA separa decisiones con dueño, fecha y motivo; se confirman antes de cerrar.
- A5 `ritual-cierre` — plantilla y regla de leer las decisiones en voz alta al final.

### A2. Cierre explícito dentro de la reunión (`cierre-explicito`)
Propuesta visible, voto u objeción anónimos y bien contados, decisión registrada con quién la tomó. Ataca converger y decidir. Persona: Joaquín Lemos (primary). Venía aparcada de la primera exploración.

### B1. El responsable confirma su compromiso (`acuse-de-compromiso`)
Al terminar, cada responsable recibe *su* compromiso (qué, para cuándo, por qué) y lo confirma o corrige en menos de 24 horas. Verifica quien recibe, no el líder. Ataca "cada uno se fue con su versión" y a quien no estuvo en la reunión. Personas: Beatriz Olmedo (primary), Hernán Soto (secondary). Reemplaza el correo que nadie confirma.

### B2. Registro de decisiones de la serie (`registro-decisiones-serie`)
Cada serie o canal tiene un registro de decisiones que se abre solo al empezar la reunión siguiente. Ataca retomar. Persona: Joaquín Lemos (primary). Reemplaza el Miro por trimestre y las capturas en Confluence.

### B3. Propuesta escrita antes de la reunión (`propuesta-previa`) — no es software
Lo que se va a decidir llega escrito antes, con opciones y recomendación; la reunión aprueba u objeta. Ataca la ambigüedad en el origen. Personas: Beatriz Olmedo (primary), Hernán Soto (secondary).

### B4. Escriba rotativo (`escriba-rotativo`) — no es software; lo más chico que podría funcionar
En cada reunión, alguien que no es el líder anota las decisiones en vivo (quién, qué, para cuándo) en las notas de la serie. Delega el registro. Personas: Hernán Soto (secondary), Beatriz Olmedo (primary). Reemplaza al líder que escribe y modera a la vez.

## Comparación

| Alternativa | Deseable | Factible | Viable | Creencia más riesgosa |
|---|---|---|---|---|
| A2 `cierre-explicito` | mixed — el líder decide al acabarse el tiempo 6/10, votos sin confianza (`real`); pero "votar no decide" (Javier) y Hernán saca las decisiones de la reunión grande (`real`) | to check with tech | unknown | Un voto u objeción anónimo y bien contado hace aparecer el desacuerdo dentro de la reunión: se reabren menos decisiones después |
| B1 `acuse-de-compromiso` | mixed — ataca el fallo del receptor que A1 no cubre: Andrés/Guayaquil, Ricardo/Postgres, México leyó el recap, squad de Paula (`real`); no quita la transcripción (8/10) y depende de una captura previa (A1, A5 o B4) | to check with tech | unknown | Los responsables confirman o corrigen su compromiso en <24 h y las discrepancias aparecen antes de ejecutar: ≥70% responde y ≥1 de cada 10 corrige algo |
| B2 `registro-decisiones-serie` | mixed — retomar duele: 5/10 perdieron lo nativo, Martina reabrió una discusión, Tomás y Javier siguen en Miro por la continuidad (`real`); continuidad 18% de las abiertas (`survey`); depende de captura previa y de la persistencia de A3 | to check with tech | unknown | Los equipos abren el registro al empezar la reunión siguiente en ≥50% de las reuniones de la serie, y se reabren menos decisiones cerradas |
| B3 `propuesta-previa` | weak — las pérdidas más caras ocurrieron después de decidir: el PRD de Sofía existía y la decisión se perdió en un comentario resuelto; las de Martina y Tomás surgieron en la reunión (`real`); a favor, 1 mención (R-131, `survey`) y Paula en reuniones chicas | strong — proceso sobre Docs/Loop existentes | weak (`assumption`) | Los líderes preparan la propuesta antes en ≥60% de las reuniones de decisión, y esas decisiones se pierden menos |
| B4 `escriba-rotativo` | mixed — las notas de Micaela "funcionan bien" (Paula) y Lucía pierde el hilo al escribir y moderar (`real`); pero el hilo de Slack de Javier existía y México igual entendió otra cosa, y el paso a Jira sigue en el líder | strong — notas de la reunión existentes | weak (`assumption`) | Un participante que no es el líder registra con calidad suficiente para que el líder no lo reescriba en ≥60% de las reuniones |

Ninguna llega a `strong` en deseable: el primer set ya se llevó el mecanismo con más evidencia (A1). B1 y B2 complementan a A1, no compiten con ella.

## Decisión

**Recomendación de la IA:** probar solo B1 dentro del prototipo de A1 (único fallo que ni A1 ni A5 cubren, costo marginal casi nulo); B4 aparcada como plan B si el piloto de A5 muestra que el líder no sostiene el cierre.

**Elegido por el usuario (2026-09-30): B1 y B4 en paralelo** (`testing-several`). Difiere de la recomendación en B4: se prueba ya, en vez de esperar al resultado de A5.

- **Prueba de B1 — dentro del prototipo "de mago" de A1:** después de que el líder confirma las decisiones, cada responsable recibe su compromiso (qué, para cuándo, por qué) y se le pide confirmar o corregir. Se mide el % que responde en <24 h y el % que corrige algo. Resuelve `[feature: acuse-de-compromiso] [value]`.
- **Prueba de B4 — como segundo brazo del piloto de 4 semanas de A5:** la mitad de los líderes cierra ellos mismos (A5); la otra mitad designa un escriba rotativo que anota en las notas de la serie. Se mide en qué % de reuniones el líder reescribe el registro y si las decisiones se retoman en la reunión siguiente. Resuelve `[feature: escriba-rotativo] [value]` y compara directamente con A5.

**Qué cambiaría la decisión:** si el brazo de B4 muestra que el líder reescribe igual lo que anotó el escriba, B4 se descarta y A5 queda sola; si B1 muestra baja respuesta de los responsables, se descarta sin costo; si la telemetría muestra muchos artefactos huérfanos, sube B2.

## Propuesta de valor: B1 `acuse-de-compromiso`

Contra Beatriz Olmedo (primary) y Hernán Soto (secondary):

- **Dolor que alivia:** el responsable entendió otra cosa o no estaba, y nadie se entera hasta que es tarde: un cliente 4 días sin atención (Andrés), dos días de arreglos y un fin de semana de guardia (Ricardo), dos semanas de retraso y una release movida (Javier) (`real`).
- **Ganancia:** el desacuerdo sobre quién hace qué aparece al día siguiente, no en la reunión de la semana que viene; el líder sabe quién aceptó qué.
- **Reemplaza:** el correo de acuerdos que se da por leído; se cambia porque el receptor tiene que confirmar, y la ambigüedad sale a la luz sola.
- **Deliberadamente no:** no captura las decisiones (depende de A1, A5 o B4); no hace seguimiento del cumplimiento ni recordatorios; no reemplaza a Jira.

## Propuesta de valor: B4 `escriba-rotativo`

Contra Hernán Soto (secondary) y Beatriz Olmedo (primary):

- **Dolor que alivia:** el líder escribe y modera a la vez y pierde el hilo (Lucía, `real`); 8 de 10 cargan solos con el registro: *"nadie más lo hace"* (`real`).
- **Ganancia:** el líder conduce y el registro se hace igual, en vivo, visible para todos.
- **Reemplaza:** la transcripción del líder durante y después de la reunión; se cambia porque reparte un trabajo invisible que hoy recae siempre en la misma persona.
- **Deliberadamente no:** no automatiza nada ni construye software; no resuelve el paso a Jira (sigue siendo manual); no resuelve la persistencia de las notas si la serie se recrea.

## Creencias

- [opportunity: decisiones-perdidas-en-reunion] [value] (#11 en product/overview.md, tal como está registrada)
- [opportunity: decisiones-perdidas-en-reunion] [viability] (#12 en product/overview.md, tal como está registrada)
- [feature: acuse-de-compromiso] [value] Cuando cada responsable recibe su compromiso (qué, para cuándo, por qué) después de la reunión, ≥70% lo confirma o corrige en menos de 24 horas y al menos 1 de cada 10 corrige algo que el registro tenía mal o ambiguo. — propuesta
- [feature: escriba-rotativo] [value] Cuando un participante que no es el líder registra las decisiones en vivo en las notas de la serie, el líder no reescribe ese registro en ≥60% de las reuniones durante 4 semanas. — propuesta

## Descartadas o aparcadas

- A2 `cierre-explicito` — parked: sigue esperando el piloto de A5 (y ahora el brazo de B4); vuelve si alguno muestra que los líderes sostienen un cierre explícito pero el desacuerdo sigue apareciendo tarde.
- B2 `registro-decisiones-serie` — parked: depende de que la captura funcione (A1) y de la persistencia en la serie (dependencia ya anotada para tech); vuelve si A1 funciona y la telemetría muestra muchos artefactos huérfanos.
- B3 `propuesta-previa` — discarded: la evidencia muestra que las decisiones se pierden después de tomarlas, no por falta de una propuesta previa; en el caso de Sofía el documento existía y la decisión igual se perdió.
