---
status: framed
parent: colaboracion-viva-en-reunion
segment: Team Leads y mandos medios que conducen reuniones de serie en cuentas Business Premium, ≥100 licencias, sector tecnología, operación en 3+ países, facturación >USD 100M anual (12.400 cuentas, 2,1M licencias)
personas: camila-reyes-aguirre, agnieszka-wrobel
---

# Oportunidad: Las decisiones de la reunión se pierden antes de llegar a la ejecución

Los Team Leads de cuentas tech grandes y distribuidas cierran reuniones sin que lo decidido quede registrado de forma confiable —con dueño, fecha y motivo, y en el lugar donde vive el trabajo—, y lo pagan en días o semanas de trabajo rehecho; hoy lo compensan transcribiendo a mano después de cada reunión o confiando en un resumen de IA que mezcla lo decidido con lo conversado. Es ahora relevante porque la evidencia de la oportunidad padre (`colaboracion-viva-en-reunion`) mostró que este es el dolor que más se repite (10 de 10 entrevistas), por encima del lienzo visual, y porque el resumen de IA ya ocupa el lugar del acta en una parte del segmento sin ganarse su confianza.

**Rama de:** [colaboracion-viva-en-reunion](2026-09-16-0526-colaboracion-viva-en-reunion.md). Cubre la secuencia **converger → decidir → registrar → retomar**.

## Segmento y personas

- **Camila Reyes Aguirre** (tipo sin registrar) — la sufre: su objetivo explícito es *"un solo lugar de verdad para decisiones técnicas, en vez de reconstruirlas cruzando Teams, Jira y Miro"* (synthetic).
- **Agnieszka Wróbel** (primary) — la sufre: quiere que las decisiones de calidad queden en un solo lugar revisable por Auditoría; Seguridad le bloqueó Miro, así que lo nativo es su única opción (synthetic).
- **Marina Ibarra Solís** (tipo sin registrar) — análogo de comportamiento fuera del segmento exacto; no se usa como evidencia.
- **Diego Farfán** (tipo sin registrar) — no la sufre como conductor, pero es quien recibe el registro; podría informar si un registro confirmado cambia lo que hace el que no habló.
- **Renata Schulz** (tipo sin registrar, admin) — no la sufre; relevante si la solución escribe en Jira/Planner (permisos, privacidad).
- **Falta:** una persona del lado comercial/CSM que explique el vínculo con renovación y upgrade (hueco heredado del padre).

## Señales

| Señal | Procedencia | Fuente |
|---|---|---|
| 10 de 10 entrevistados contaron una decisión perdida con costo concreto: de un acuerdo que se rediscute a dos semanas de retraso y una release movida | real | product/insights/2026-09-30-0211-colaboracion-en-vivo-entrevistas.md |
| 8 de 10 escriben el registro a mano después de la reunión, 10 a 60 minutos por reunión: *"nadie más lo hace"* | real | ídem |
| El resumen de IA falla como acta en los 6 de 6 que lo usan (mezcla decisión con conversación, sin dueño ni fecha, no ve el artefacto); causó directamente 2 de los errores | real | ídem |
| 6 de 10: decide el líder cuando se acaba el tiempo; 3 no saben si el grupo estaba de acuerdo | real | ídem |
| En el 24% de las reuniones que trabajaron afuera lo decidido no quedó registrado (igual en los dos canales); otro 23% quedó en un chat fuera de Teams | survey, n=182 | product/insights/2026-09-30-0205-colaboracion-en-vivo-fuera-de-teams.md |
| El 14% dejó lo decidido en el resumen de IA, la transcripción o la grabación; 13 de esos 26 agregan una queja sin que se les pregunte | survey, n=182 | ídem |
| Registro y seguimiento (20%) y continuidad entre reuniones (18%) son los dos temas más mencionados en las respuestas abiertas | survey, n=79 | ídem |
| Las actividades que más se hacen afuera son decidir y registrar (votar o priorizar 40%, anotar decisiones 33%), no las de pizarra | survey, n=182 | ídem |
| El resumen de IA es la función nativa más adoptada (36%); 39% la conoce y nunca la usó | survey, n=210 | ídem |
| El grupo que no trabaja afuera decide con recursos improvisados (manos alzadas, Excel dictado, notas en el chat): *"si no lo anoto yo no lo anota nadie"* | survey, n=16 (direccional) | ídem |

## Resultado de negocio

El mismo del padre: tasa de upgrade a Max, retención en la renovación e ingreso por licencia. El vínculo específico de esta rama es que el resumen de IA ya es la función nativa más usada y el plan Max se vende por "capacidades avanzadas de reuniones" (overview): un registro de decisiones confiable podría ser un motivo de upgrade. No hay evidencia de ese vínculo todavía.

## Restricciones

Heredadas del padre: presupuesto máximo USD 5M; exhibición en CollabCon (≈ mediados de febrero de 2027); facilidad de uso, accesibilidad, compatibilidad con Microsoft 365, privacidad y seguridad corporativas, tiempo real e impacto mínimo en el rendimiento. Se agrega: en cuentas del EEE con restricciones de compliance, el registro tiene que quedar dentro de Microsoft 365 (5 menciones, direccional).

## Creencias

Registradas en `product/overview.md`:

- [opportunity: decisiones-perdidas-en-reunion] [value] En las reuniones de serie del segmento, lo decidido se pierde entre la reunión y la ejecución con un costo que el líder puede nombrar: en ≥20% de las reuniones no queda un registro utilizable de la decisión, y el líder dedica ≥10 minutos por reunión a transcribirla a mano.
- [opportunity: decisiones-perdidas-en-reunion] [viability] Las cuentas del segmento cuyos Team Leads usan el resumen de IA de forma sostenida renuevan o suben a Max en mayor proporción que las que no: el registro de decisiones es una capacidad por la que el segmento paga.
- Hereda del padre, por referencia: [opportunity: colaboracion-viva-en-reunion] [viability] (#4).

## Agenda de investigación

| Creencia | Instrumento | Decisión que desbloquea | Para cuándo |
|---|---|---|---|
| [value] | Datos del producto: en reuniones de serie del segmento, % con resumen de IA generado, % compartido o editado después, y % con notas o tareas creadas en la reunión | Dimensionar el dolor en el segmento completo, no solo en la muestra | 2–3 semanas |
| [value] | Entrevistas con el grupo que no trabaja afuera (R-120, R-046, R-009, R-085, R-088, R-242, R-135) | Confirmar que el dolor existe también donde no hay Miro ni Jira de por medio | 3–4 semanas |
| [viability] | Datos del producto: cruzar uso sostenido del resumen de IA en el segmento contra resultado de renovación y upgrade a Max en 12 meses | Si esta rama se presenta en CollabCon como motor de upgrade o como defensa de retención | 4–6 semanas |
| [viability] | Conversación con ventas/CSM sobre las menciones de "colaboración" en renovaciones de Max | Llenar el hueco de la persona comercial | 2 semanas |

## Ideas candidatas

Ya exploradas en [product/solutions/2026-09-30-0314-colaboracion-viva-en-reunion.md](../solutions/2026-09-30-0314-colaboracion-viva-en-reunion.md), hecha contra este problema antes del reencuadre:

- `recap-decisiones-confirmable` (A1) — **chosen**, en prueba.
- `ritual-cierre` (A5) — **chosen**, en piloto.
- `cierre-explicito` (A2) — **parked**, vuelve si el piloto de A5 sale bien. Reevaluada en [soluciones 2](../solutions/2026-09-30-0339-decisiones-perdidas-en-reunion.md): sigue **parked**.

Segunda exploración en [soluciones 2](../solutions/2026-09-30-0339-decisiones-perdidas-en-reunion.md) (2026-09-30), con mecanismos nuevos:

- `acuse-de-compromiso` (B1) — **chosen**, se prueba dentro del prototipo de A1.
- `escriba-rotativo` (B4) — **chosen**, segundo brazo del piloto de A5.
- `registro-decisiones-serie` (B2) — **parked**, depende de que la captura de A1 funcione y de la persistencia en la serie.
- `propuesta-previa` (B3) — **discarded**: las decisiones se pierden después de tomarlas, no por falta de propuesta previa.
