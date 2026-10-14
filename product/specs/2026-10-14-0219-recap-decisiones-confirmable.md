---
feature: recap-decisiones-confirmable
opportunity: decisiones-perdidas-en-reunion
solutions: product/solutions/2026-09-30-0314-colaboracion-viva-en-reunion.md (A1)
tests: product/tests/2026-10-07-0151-decisiones-perdidas-en-reunion.md (T1, T2 — sin correr)
status: approved
date: 2026-10-14
revised: 2026-10-14 — tras el panel product/insights/2026-10-14-0238-critique-recap-decisiones-confirmable.md (mejoras 1 y 2: salida mínima al ticket e historia de administración)
---

# Resumen de decisiones confirmable

## Problema

Los Team Leads que conducen reuniones de serie salen de la llamada sin un registro confiable de lo decidido. Lo transcriben ellos mismos después, de 10 a 60 minutos por reunión, o confían en el resumen de IA, que mezcla lo decidido con lo conversado. El costo es concreto: en las 10 entrevistas hubo una decisión perdida que costó de días a semanas de trabajo. Es el momento porque el resumen de IA ya es la función nativa más usada (36%) y ya hace de acta en parte del segmento, pero no se gana su confianza: falla en los 6 de 6 entrevistados que lo usan.

> Evidencia: *"En la reunión se acordó, con fecha. En el recap quedó como 'se habló de la API de geocercas'. El equipo de México leyó el recap, no el hilo… Entregaron dos semanas tarde."* — Javier Molina, product/interviews/2026-09-28-0900-javier-molina.md
>
> *"Marca como decisión cosas que eran solo ideas… Perdimos más o menos una semana de dos desarrolladores."* — Paula Benítez, product/interviews/2026-09-28-1400-paula-benitez.md
>
> *"Lo paso yo a Jira, a mano… Me lleva unos veinte minutos… Nadie más lo hace."* — Tomás Aguirre, product/interviews/2026-09-25-1000-tomas-aguirre.md
>
> 10 de 10 con decisión perdida y costo concreto; 8 de 10 transcriben a mano — product/insights/2026-09-30-0211-colaboracion-en-vivo-entrevistas.md (`real`). 24% de las reuniones sin registro — product/insights/2026-09-30-0205-colaboracion-en-vivo-fuera-de-teams.md (`survey`, n=182).

## Para quién

- **Joaquín Lemos** (primary, elegido como persona del recorrido) — conduce retros y plannings de serie con 10 a 14 personas en 3 o 4 países, y después pasa de 20 minutos a una hora copiando acuerdos; para él, retomar los acuerdos en la sesión siguiente es la razón de usar Miro.
- **Beatriz Olmedo** (primary) — escribe el registro a mano después y pierde el porqué y el quién. Su deseo explícito es que la decisión "quede en el ticket": en esta versión no hay integración con el ticket, pero cada decisión se puede copiar lista para pegar, con el motivo y el enlace al registro (ver *Deliberadamente no*). Su valor sigue a medias.
- **Agnieszka Wróbel** (primary, nombrada en la propuesta de valor de A1) — en cuentas con compliance, lo nativo es su única opción; el registro tiene que quedar dentro de Microsoft 365.
- **Renata Schulz** (tertiary) — administra Microsoft 365: decide si la función se habilita y tiene que justificar su costo ante Finanzas. No usa la función; la permite o la bloquea.

La propuesta de valor de A1 se escribió contra Camila Reyes Aguirre y Agnieszka Wróbel; esta spec usa a Joaquín como persona del recorrido por decisión del usuario (2026-10-14), porque es una persona derivada de entrevistas reales.

### Deliberadamente no

- **No se integra con Jira ni con Planner en esta versión.** El registro confirmado queda en la serie y se publica en el canal. Decisión del usuario (2026-10-14): reduce el riesgo técnico, pero se aparta de la propuesta de valor de A1 ("lo envía adonde vive el trabajo"). **Salida mínima** (revisión tras el panel): cada decisión confirmada se puede copiar como texto listo para pegar en un ticket, con qué, responsable, fecha, motivo y enlace al registro. El ticket lo sigue creando el líder, pero ya no reescribe la decisión.
- No es un lienzo ni una pizarra; no vota ni facilita la discusión; no decide por el grupo: propone y el grupo confirma.
- No pide a cada responsable que confirme su compromiso: eso es B1 `acuse-de-compromiso`, con spec propia.
- No ve lo que pasa en herramientas externas (Miro, FigJam): solo lo que se dice en la reunión.

## Recorrido del usuario

Recorrido de Joaquín en una retro o planning de serie, según Tomás, Javier y Valeria (product/personas/joaquin-lemos.md):

1. **Disparador** — Joaquín conduce la retro de la serie con 11 personas en tres países. El objetivo es salir con dos o tres acuerdos (Tomás) o con las prioridades del trimestre (Javier, Valeria).
2. **Facilita y el grupo converge** — Pega el link del tablero, el grupo aporta, agrupa y vota. Cuando la discusión se traba, decide él porque se acaba la hora (Tomás, Javier: 6 de 10). Lo decidido en el tablero solo lo capta el registro si alguien lo dice en voz alta (supuesto #19).
3. **Los últimos minutos: aparece la lista de decisiones** *(punto de dolor; hoy "nadie anotó nada en el momento", Valeria)*. Antes de cortar, Joaquín abre en Teams la lista de decisiones que propone el sistema, separada del resumen de lo conversado: cada decisión con qué, responsable, fecha y motivo. Si a alguna le falta un campo, aparece marcado como vacío.
4. **El grupo la revisa en pantalla** — Joaquín la comparte y la lee. Alguien dice "eso era una idea, no lo decidimos" y Joaquín la quita (el error de Paula). Otro corrige la fecha. Joaquín confirma la lista.
5. **El registro queda en la serie y en el canal** — La lista confirmada queda guardada en la serie y se publica en el canal del equipo. Hoy Javier lo hace a mano: reescribe el recap durante media hora y lo publica en el hilo de Slack y en el canal de Teams.
6. **Resultado** *(aquí llega el valor)* — Al cortar la llamada, el registro ya existe, el grupo lo confirmó y Joaquín no tiene que reescribirlo. Quien no estuvo lo lee en el canal.
7. **Retomar** — En la retro siguiente de la serie, aunque la serie se haya recreado, Joaquín abre los acuerdos anteriores y pregunta "¿esto lo cumplimos?" (Tomás). Hoy, la pizarra nativa se pierde justo en este paso (5 de 10).

Fuera del recorrido en esta versión: Joaquín sigue creando los tickets en Jira, pero copia cada decisión ya escrita, con su motivo y el enlace al registro, en vez de reescribirla a partir de capturas (Tomás: 20 minutos; Valeria: casi una hora y una decisión mal cargada).

## Historias críticas

### Ver las decisiones propuestas antes de cerrar

Como Joaquín Lemos, quiero ver antes de cortar la llamada una lista con solo lo que se decidió, cada decisión con responsable, fecha y motivo, para no tener que reconstruirlo después a partir de la grabación o del resumen.

Criterios de aceptación:
- [ ] Durante la reunión, el organizador puede abrir la lista de decisiones propuestas sin salir de Teams.
- [ ] La lista aparece separada del resumen de lo conversado y solo contiene los puntos que alguien acordó de forma explícita en la reunión.
- [ ] Cada decisión muestra cuatro campos: qué, responsable, fecha y motivo.
- [ ] Si falta un campo, aparece como "sin responsable", "sin fecha" o "sin motivo", y no se completa con un dato inventado.
- [ ] Caso límite: una propuesta sin cierre ("podríamos pasar el release al 20") no aparece como decisión.

Se basa en: insights …0211 #1 y #2 (Javier, Paula, Martina, Lucía).

### Corregir y confirmar con el grupo

Como Joaquín Lemos, quiero corregir la lista y confirmarla con el grupo antes de cerrar, para que lo registrado sea lo que todos acordaron y no mi versión.

Criterios de aceptación:
- [ ] El organizador puede quitar, agregar y editar una decisión y cada uno de sus cuatro campos.
- [ ] La lista se puede mostrar a todos los participantes dentro de la reunión, sin que tengan que abrir otra aplicación.
- [ ] Al confirmar, el registro guarda quién confirmó y a qué hora, y queda marcado como "confirmado".
- [ ] Caso límite: si la reunión termina sin confirmar, la lista queda marcada como "sin confirmar", el organizador puede confirmarla después y la marca muestra que se confirmó fuera de la reunión.

Se basa en: insights …0211 #2 y #5 (Paula: ideas registradas como decisiones; Martina, Sofía: no saben si el grupo estaba de acuerdo).

### El registro vive en la serie y sobrevive a recrearla

Como Joaquín Lemos, quiero encontrar los acuerdos de la sesión anterior al abrir la siguiente reunión de la serie, para retomar donde quedamos.

Criterios de aceptación:
- [ ] Los registros confirmados se pueden abrir desde la serie de reuniones, ordenados por fecha de reunión.
- [ ] Al empezar la siguiente reunión de la serie, el organizador ve un acceso al último registro confirmado.
- [ ] Caso límite: si la serie se reprograma o se recrea con otra invitación, los registros anteriores siguen apareciendo en la nueva.
- [ ] El registro se guarda dentro de Microsoft 365, sin salir del espacio de la cuenta.

Se basa en: insights …0211 #3 (Tomás, Paula, Lucía: 5 de 10 perdieron el registro al recrear la serie); restricción de compliance de la oportunidad.

### Publicar el registro confirmado y llevarlo al ticket

Como Joaquín Lemos, quiero publicar en el canal del equipo el registro confirmado en un paso, y llevar cada decisión al ticket sin reescribirla, para que quien no estuvo o no habló sepa qué se decidió y para que el porqué llegue adonde se ejecuta.

Criterios de aceptación:
- [ ] Con una sola acción, el organizador publica el registro confirmado en el canal de Teams asociado a la serie.
- [ ] La publicación muestra solo las decisiones con sus cuatro campos, sin el resumen de lo conversado.
- [ ] La publicación tiene un enlace al registro de la serie.
- [ ] Un miembro del canal que no asistió a la reunión puede leer la publicación.
- [ ] Caso límite: un registro "sin confirmar" no se puede publicar sin que el organizador lo confirme antes.
- [ ] Cada decisión confirmada tiene una acción "copiar para ticket" que copia al portapapeles qué, responsable, fecha, motivo y el enlace al registro de la serie, en texto plano que se puede pegar en Jira, Azure DevOps o Planner.

Se basa en: insights …0211 #1 (Javier publica a mano en el canal; Sofía: "que lo sepan todos, incluso los que no hablaron"; México leyó el recap y no el hilo; Tomás y Valeria pasan los acuerdos a Jira a mano); Martina: "que eso quede en el ticket" (insights …0211 #2).

### Habilitar la función y saber cuánto se usa

Como Renata Schulz, quiero controlar dónde está habilitada la función, que respete las políticas que ya tengo y ver cuánto se usa, para poder permitirla sin riesgo y justificar su costo ante Finanzas.

Criterios de aceptación:
- [ ] En el centro de administración de Microsoft 365, la administradora puede habilitar o deshabilitar la función por grupo de usuarios.
- [ ] Los registros de decisiones quedan sujetos a las mismas políticas de retención y de eDiscovery que ya tiene configuradas para las reuniones.
- [ ] Caso límite: si la transcripción está desactivada por política en una reunión, no se ofrece la lista de decisiones y el organizador ve un mensaje que explica por qué.
- [ ] Antes de publicar en un canal que tiene invitados externos, el organizador ve un aviso que lo dice y tiene que confirmar para publicar.
- [ ] La administradora ve un reporte de uso por grupo y período: reuniones con lista generada, con lista confirmada y con registro publicado.

Se basa en: persona Renata Schulz (frustraciones sobre el upgrade a Max y la falta de datos de uso); restricción de compliance de la oportunidad (el registro dentro de Microsoft 365); panel de crítica product/insights/2026-10-14-0238-critique-recap-decisiones-confirmable.md (`synthetic`). Sin evidencia `real`: queda como supuesto #21.

## Hipótesis

Creemos que los Team Leads del segmento que conducen reuniones de serie con decisiones van a **publicar el registro confirmado sin edición sustantiva** en al menos el 60% de esas reuniones, porque confirmarlo con el grupo antes de cerrar les quita la reescritura de 10 a 60 minutos y el riesgo de registrar ideas como decisiones.

Estamos equivocados si, en las reuniones donde se generó la lista, el líder agrega, quita o cambia una decisión, un responsable, una fecha o un motivo **después de cerrar** en más del 40% de los casos, o si sigue escribiendo su propio registro aparte (correo, hilo, recap reescrito) en más de la mitad de las reuniones.

(Misma definición de "edición sustantiva" que T1: cambiar la redacción no cuenta.)

## Alternativas consideradas

Exploradas en: product/solutions/2026-09-30-0314-colaboracion-viva-en-reunion.md y product/solutions/2026-09-30-0339-decisiones-perdidas-en-reunion.md
- A5 `ritual-cierre` — elegida en paralelo, en prueba (T4): la misma conducta de cierre, sin software.
- A2 `cierre-explicito` — aparcada: depende de lo que muestre el piloto de A5.
- A3 `whiteboard-persistente` — aparcada: dolor real pero secundario; su pieza de persistencia en la serie pasa a esta spec (historia 3).
- A4 `artefacto-en-reunion` — aparcada: ataca la participación, no el registro.
- Acceso de invitados externos — aparcada: es de otro segmento.
- B1 `acuse-de-compromiso` — elegida, en prueba (T3) y con spec aparte: depende de esta captura.
- B4 `escriba-rotativo` — elegida, en prueba (T5): delega el registro en una persona en vez de en la IA.
- B2 `registro-decisiones-serie` — aparcada: depende de que esta captura funcione.
- B3 `propuesta-previa` — descartada: las decisiones se pierden después de tomarlas.

## Probado antes de la spec

Probado en: product/tests/2026-10-07-0151-decisiones-perdidas-en-reunion.md
- **La creencia más riesgosa no está probada (declarado).** El usuario decidió escribir la spec antes de correr las pruebas (2026-10-14).
- T1 tarjeta de decisiones hecha a mano — sin correr (`ready`) · #8 [value]. Aun cuando corra, prueba la tarjeta *después* de la reunión, no la confirmación *antes* de cerrar que describe esta spec.
- T2 extracción automática contra las tarjetas de T1 — sin correr (`designed`) · #9 [feasibility]. Depende de T1.
- La revisión tras el panel (copiar para ticket, historia de administración) no cambia lo que miden T1 ni T2.
- Cambio respecto de lo diseñado: esta spec deja Jira y Planner fuera de esta versión. T1 no medía el envío a Jira, así que su diseño sigue valiendo; la parte de #9 sobre el envío a Jira/Planner no aplica a esta versión.

## Supuestos

Registrados en `product/overview.md`:
- [feature: recap-decisiones-confirmable] [value] (#8) Cuando un Team Lead del segmento ve las decisiones extraídas (dueño, fecha, motivo) y las confirma antes de cerrar la reunión, deja de reescribir el registro después: en ≥60% de las reuniones el registro confirmado se envía sin edición sustantiva.
- [feature: recap-decisiones-confirmable] [feasibility] (#9) Se pueden separar decisiones de conversación, con dueño y fecha, con precisión suficiente para que el líder no las reescriba, y enviarlas a Jira/Planner y a la serie, dentro del plazo de CollabCon y las restricciones de rendimiento y privacidad. — to check with tech
- [opportunity: decisiones-perdidas-en-reunion] [value] (#11) y [viability] (#12), tal como están registradas.

Agregados desde esta spec (2026-10-14, #17 a #20):
- [feature: recap-decisiones-confirmable] [value] (#17) Aunque el registro confirmado no llegue a Jira ni a Planner, los líderes que hoy pasan los acuerdos a mano reducen al menos a la mitad el tiempo que dedican a registrar después de la reunión.
- [feature: recap-decisiones-confirmable] [usability] (#18) El grupo revisa y confirma la lista en los últimos minutos sin alargar la reunión más de 3 minutos, y el líder la confirma dentro de la reunión en al menos el 70% de los casos.
- [feature: recap-decisiones-confirmable] [usability] (#19) En reuniones donde se decide sobre un tablero externo (Miro, FigJam), el líder dice en voz alta lo decidido para que la lista lo capte; si no lo hace, faltan las decisiones tomadas en el tablero.
- [feature: recap-decisiones-confirmable] [feasibility] (#20) El registro confirmado puede quedar asociado a la serie, y no a la instancia de la reunión, y seguir apareciendo cuando la serie se reprograma o se recrea. — to check with tech

Agregado tras el panel (2026-10-14, #21):
- [feature: recap-decisiones-confirmable] [viability] (#21) Los administradores de Microsoft 365 del segmento habilitan la función cuando respeta sus políticas de retención y transcripción y viene con un reporte de uso.

Decisión abierta: en qué plan va la función (Premium o Max). Depende de #12 y #21; sin decidir.
