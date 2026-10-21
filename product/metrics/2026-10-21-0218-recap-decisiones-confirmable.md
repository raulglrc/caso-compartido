---
spec: product/specs/2026-10-14-0219-recap-decisiones-confirmable.md
exposure-plan: product/exposure-plans/2026-10-14-0248-recap-decisiones-confirmable.md
level: 1 — Ver las decisiones propuestas
status: designed
---

# Métricas de: Resumen de decisiones confirmable

## Audiencia objetivo

**Quiénes cuentan:** los organizadores de reuniones de serie que cumplen las tres condiciones siguientes durante las 2 semanas del Nivel 1:
- pertenecen a una cuenta del segmento (tech grande y distribuido: Business Premium, ≥100 licencias, sector tecnología, 3+ países, >USD 100M; 12.400 cuentas);
- el administrador de su cuenta habilitó la función para su grupo;
- condujeron al menos una reunión de serie con transcripción activa en la que se generó una lista con al menos una decisión propuesta.

**Fuentes:** el segmento viene de `product/overview.md`; la audiencia, del Nivel 1 del plan de exposición.

**Tamaño:** desconocido. Se conoce el número de cuentas, pero no el de organizadores elegibles; se fija al cerrar el nivel.

**Organizador o participante:** en el Nivel 1 solo cuenta el **organizador**, porque es el único que ve la lista. Los participantes entran como audiencia propia en el Nivel 2, cuando la lista se muestra a todos.

**Con el mecanismo incremental**, la función llega a toda la población, pero el denominador se filtra al segmento en el análisis (pregunta abierta del plan, aquí resuelta así).

## Frecuencia esperada

**Semanal.** El 52% de quienes trabajaron afuera conduce 2 o 3 reuniones por semana y el 38%, 4 o más (`survey`, R2, product/insights/2026-09-30-0205-colaboracion-en-vivo-fuera-de-teams.md). Las entrevistas coinciden: entre 2 y 6 reuniones grandes por semana (`real`).

No todas esas reuniones tienen decisiones: el review de Paula no decide nada a propósito. Se toma como unidad **al menos una reunión de serie con decisiones por semana**, el mismo criterio con el que se recluta para T1. La ventana de retención es la semana.

## Acquisition

- **Señal:** el organizador abre la lista de decisiones propuestas **durante** la reunión, antes de que termine.
- **Definición ampliada:** cuenta cada organizador de la audiencia que la abrió al menos una vez durante una reunión elegible en las 2 semanas. No cuenta abrirla después de que terminó la reunión: el plan mide el cierre.
- **Cálculo:** organizadores que abrieron la lista durante la reunión / audiencia objetivo, en las 2 semanas del nivel.
- **Lectura complementaria (para el plan):** reuniones elegibles en que el organizador abrió la lista antes del final / reuniones elegibles.
- **Meta:** ≥50% de la audiencia · **Por qué:** es el mismo umbral que el plan pone por reunión. Si menos de la mitad de los organizadores la abre alguna vez, la tasa por reunión tampoco puede llegar al 50%.
- **Eventos necesarios:**
  - `meeting_eligible`: meetingId, seriesId, organizerId, tenantId, segmento, transcripción activa, nivel, hora de fin programada.
  - `decision_list_generated`: meetingId, número de propuestas.
  - `decision_list_opened`: meetingId, userId, rol, timestamp, `during_meeting` (sí/no).
  - `meeting_ended`: meetingId, timestamp.
  - `feature_enabled_by_admin`: tenantId, groupId, timestamp.

## Activation

- **Señal:** el organizador abre la lista durante la reunión en **2 o más reuniones distintas** de su serie, y en esas listas marca como "no es una decisión" **como mucho el 20%** de lo propuesto.
- **Definición ampliada:** cuenta el organizador de la audiencia, con aperturas durante reuniones elegibles dentro de las 2 semanas.
- **Umbral de la señal:** segunda apertura con ≤20% de marcas · **Por qué:**
  - Volver a abrirla en otra reunión es lo que separa probarla de encontrarle valor.
  - El 20% es el umbral del plan para "la reconocen como lo que se decidió" (creencia 1). Registrar ideas como decisiones es el error que ya causó daño (Paula).
  - **Excluye:** una sola apertura; aperturas después de la reunión; listas con más del 20% marcado.
- **Cálculo:** organizadores activados / audiencia objetivo.
- **Lectura complementaria (para el plan):** decisiones marcadas como "no es una decisión" / decisiones propuestas, sobre todas las listas abiertas.
- **Meta:** ≥35% de la audiencia · **Por qué:** es aproximadamente el 70% de quienes llegan (meta de acquisition 50% × 70% de conversión). El plan no fija meta de activación; esta es una propuesta.
- **Eventos necesarios:** los de acquisition, más:
  - `decision_marked_not_decision`: meetingId, decisionId, userId, timestamp.

## Retention

- **Señal:** el organizador abre la lista durante la reunión en al menos una reunión elegible **por semana**.
- **Definición ampliada:** organizadores activados que la abren en las dos semanas del nivel. Solo cuentan las semanas en que condujeron una reunión elegible; una semana sin reunión elegible no se cuenta como abandono.
- **Curva de retención:** cohortes por semana de la primera apertura durante la reunión, seguidas semana a semana.
  - Con 2 semanas, la lectura es **direccional**.
  - La curva completa se lee a medida que la misma audiencia pasa a los niveles 2 a 4 (≈10 semanas).
- **Cálculo:** organizadores que abren la lista en las dos semanas en que tuvieron reunión elegible / audiencia objetivo.
- **Meta:** ≥30% de la audiencia · **Por qué:** es cerca del 85% de los activados. En un nivel de 2 semanas, perder más de eso entre la semana 1 y la 2 indica que el segundo uso es peor que el primero.
- **Eventos necesarios:** los de acquisition (alcanza `decision_list_opened` con `during_meeting` y la semana de `meeting_eligible`).

## Satisfaction

- **Instrumento:** CSAT dentro de la app.
- **Pregunta:** "¿Qué tan bien refleja esta lista lo que se decidió en la reunión?" (1 a 5), con un campo opcional: "¿Qué faltó o qué sobró?"
- **Cuándo aparece:** al cerrar la lista la **segunda vez** que el organizador la abre durante una reunión. Una vez por persona en el nivel.
- **Corte:** 4 o 5.
- **Definición ampliada:** organizadores de la audiencia que respondieron 4 o más.
- **Cálculo:** organizadores con 4 o más / audiencia objetivo. La tasa de respuesta y el porcentaje entre quienes respondieron se informan aparte. Con menos del 30% de respuesta, la lectura es direccional.
- **Meta:** ≥25% de la audiencia (≈70% de los activados) · **Por qué:** quien no reconoce la lista como lo decidido no va a confirmarla en el Nivel 2.
- **Eventos necesarios:**
  - `csat_shown`: userId, meetingId, nivel.
  - `csat_answered`: userId, score, comentario, timestamp.

## Métricas de negocio

Declaradas en `product/overview.md`, tal como están:
- **Las métricas que mira dirección para el segmento:** tasa de upgrade a Max, retención en la renovación e ingreso por licencia.
- **[viability] #12:** las cuentas cuyos Team Leads usan el resumen de IA de forma sostenida renuevan o suben a Max en mayor proporción.
- **[viability] #4:** resolver la sustitución mueve al menos una de esas tres métricas.
- **[viability] #21:** los administradores habilitan la función cuando respeta sus políticas y trae un reporte de uso.

En las 2 semanas del Nivel 1 no se mueven las renovaciones, así que estas métricas no se leen en este nivel. Lo único observable es una señal temprana de #21: la proporción de cuentas del segmento que habilitaron la función (`feature_enabled_by_admin`). Se informa al lado, no como meta del nivel.

## Conciliación con el plan de exposición

- **Avanzar si el organizador abre la lista antes del final en ≥50% de las reuniones** → lo lee la lectura complementaria de **acquisition** (por reunión). La meta por persona (≥50%) es compatible: es una condición necesaria, no la misma medida.
- **Avanzar si ≤20% de las decisiones propuestas se marcan como "no es una decisión"** → lo lee la lectura complementaria de **activation** (tasa agregada de marcas).
- **Detenerse si se abre en <25% de las reuniones** → la misma lectura de acquisition por reunión.
- **Detenerse si se marcan >35%** → la misma lectura de activation.
- **Retention y satisfaction** no leen ningún criterio del Nivel 1. Son informativas: anticipan si vale la pena el Nivel 2.
