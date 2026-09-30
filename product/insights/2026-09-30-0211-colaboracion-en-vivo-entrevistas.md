---
source: real
sources:
  - product/interviews/2026-09-25-1000-tomas-aguirre.md (real, R-113, panel)
  - product/interviews/2026-09-25-1100-andres-quintero.md (real, R-170, panel)
  - product/interviews/2026-09-25-1600-lucia-fernandez.md (real, R-143, email)
  - product/interviews/2026-09-28-0900-javier-molina.md (real, R-097, panel)
  - product/interviews/2026-09-28-0930-martina-rojas.md (real, R-224, panel)
  - product/interviews/2026-09-28-1000-diego-paredes.md (real, R-036, email)
  - product/interviews/2026-09-28-1200-sofia-martinez.md (real, R-151, panel)
  - product/interviews/2026-09-28-1400-paula-benitez.md (real, R-153, email)
  - product/interviews/2026-09-28-1500-valeria-castro.md (real, R-024, email)
  - product/interviews/2026-09-28-1700-ricardo-salinas.md (real, R-196, panel)
excluded:
  - product/interviews/2026-09-23-0256-pretest-*.md (3 pretests sintéticos: su propio encabezado indica no pasarlos a /extract-insights)
  - product/interviews/interviews.zip (copia idéntica de los 10 archivos reales)
related: product/insights/2026-09-30-0205-colaboracion-en-vivo-fuera-de-teams.md (análisis de la encuesta)
date: 2026-09-30
---

# Insights de entrevistas: colaboración en vivo fuera de Teams

**Corpus:** 10 entrevistas reales de exploración (26 a 34 minutos), hechas entre el 25 y el 28/09 con Team Leads y managers reclutados entre quienes respondieron la encuesta. Hay 6 del panel y 4 del email, de 6 países.

**Sesgo del corpus:** 7 de los 10 entrevistados habían quedado marcados en la encuesta como candidatos que contradicen la creencia: 4 por no trabajar en herramientas externas (Q1) y 3 por usar artefactos que ya existían y entrar en menos de 2 minutos (Q4 + Q6). Así se buscó a propósito, pero hay que tenerlo en cuenta: el corpus sobrerrepresenta a quienes no sienten la necesidad de un lienzo visual. Los conteos que siguen ("n de 10") muestran cuánto se repite algo; no son proporciones del segmento.

**Dato para la encuesta:** Tomás (R-113) reconoce que en la encuesta exageró la intensidad ("puse que salgo de Teams en todas las reuniones. No es así"). Es un solo caso, pero apoya leer con cautela el grupo de intensidad alta, que está sobrerrepresentado en el panel.

## 1. La decisión se pierde entre la reunión y la ejecución, y eso cuesta semanas de trabajo

**Recurrencia: 10 de 10.** Cuando se les pidió la última vez que algo decidido terminó hecho distinto, los diez contaron un caso concreto con un costo que se puede medir: dos semanas de retraso y una release movida (Javier), dos semanas de trabajo que hubo que deshacer (Sofía), una semana de dos desarrolladores (Paula), una semana de un diseñador en algo descartado (Valeria), dos días de arreglos más un fin de semana de guardia (Ricardo), un cliente cuatro días sin atención (Andrés), una incidencia de un banco sin dueño durante una semana (Lucía), una campaña con tres días más de gasto (Diego), una discusión reabierta un mes después (Martina) y un acuerdo que se olvidó y hubo que volver a discutir (Tomás).

Las causas son distintas, pero todas caen en el mismo tramo:

- **Nadie lo escribió:** Ricardo y Tomás.
- **Se escribió tarde:** Diego mandó el correo dos días después.
- **El dueño quedó ambiguo:** Andrés y Lucía.
- **Quedó en un lugar escondido:** un comentario resuelto que se oculta (Sofía) o un hilo de Slack (Martina, con el porqué).
- **Se cargó mal desde una captura:** Valeria.
- **El resumen de IA lo registró mal:** Javier y Paula (ver el insight 2).

Además, **8 de 10** escriben ellos mismos el registro después de la reunión, a mano: correo, Jira, acta o un resumen reescrito. Les lleva entre 10 y 60 minutos por reunión, y varios lo dicen igual: *"nadie más lo hace"*. **Implicación:** el trabajo que más vale no es colaborar durante la reunión, sino cerrarla. Hace falta que la decisión quede capturada en el momento, con responsable, fecha y motivo, y que llegue sola al lugar donde vive el trabajo (el ticket, el PRD, el canal), sin que el líder la transcriba.

> Evidencia: *"En la reunión se acordó, con fecha. En el recap quedó como 'se habló de la API de geocercas'. El equipo de México leyó el recap, no el hilo, y entendió que no era prioridad. Entregaron dos semanas tarde. Nosotros tuvimos que mover una release entera."* (Javier Molina)
>
> *"Lo que nos falla es cómo se cierra la reunión: que quede claro qué se decidió, que lo sepan todos, incluso los que no hablaron. Eso lo hago medio a mano y a veces se me va."* (Sofía Martínez)

## 2. El resumen de IA ya se usa como acta, pero no distingue lo decidido de lo conversado, y ya causó errores

**Recurrencia: 6 de 6 de quienes lo usan** (Lucía, Javier, Martina, Diego, Paula y Valeria). Todos le encuentran el mismo tipo de falla. Esta vez las entrevistas explican lo que la encuesta solo cuantificaba (13 de 26 quejas en Q9). Las fallas son de tres clases:

- **Mezcla la decisión con la conversación.** Pone todo al mismo nivel (Javier), resume la charla y no lo decidido (Martina) y registra ideas como decisiones (Paula).
- **Le faltan el responsable y la fecha.** *"No me dice quién se comprometió a qué"* (Lucía).
- **No ve el artefacto.** No sabe qué filtro ni qué gráfico se estaba mirando (Diego), no ve la votación hecha en FigJam (Valeria) y no ve lo que se decidió en Slack (Martina).

En **2 casos** el resumen causó directamente el error: el retraso de dos semanas de Javier y la semana perdida de Paula. La reacción fue la misma en todos: Javier reescribe el recap en 30 minutos, Paula lo corrige en 10 y Martina lo dejó de usar. **Implicación:** es la palanca de IA más clara que apareció. Un resumen que separe las decisiones, cada una con dueño, fecha y motivo, y las muestre para confirmar antes de cerrar la reunión convierte una función que ya se usa en algo en lo que se puede confiar. Si además capta lo que pasó en el artefacto compartido (el tablero, el filtro del dashboard), cubre justo lo que hoy se pierde.

> Evidencia: *"El resumen me ahorra un montón, eh. Pero tiene un problema: marca como decisión cosas que eran solo ideas… Perdimos más o menos una semana de dos desarrolladores. Desde entonces reviso el resumen antes de mandarlo, siempre."* (Paula Benítez)
>
> *"Lo que sí me serviría es algo que cierre la reunión con lo decidido y el por qué, y que eso quede en el ticket. Eso no lo tengo."* (Martina Rojas)

## 3. Lo nativo muere con la reunión: la pizarra y las notas no sobreviven a una serie que cambia, y ahí gana Miro

**Recurrencia: 5 de 10** perdieron lo que habían hecho en la herramienta nativa. Cuatro perdieron la pizarra de Teams (Tomás, Lucía, Sofía y Ricardo) y una perdió las notas de Loop (Paula). La causa es la misma cada vez: el artefacto queda atado al chat o a la invitación de *esa* reunión, y cuando la serie se recrea, se reprograma o se convoca de nuevo, desaparece. Del otro lado, los dos que siguen en Miro dan la continuidad como el motivo principal: un tablero por trimestre, un frame nuevo por sesión y la revisión de los acuerdos anteriores (Tomás y Javier).

Además, los **5 que probaron Whiteboard** la dejaron, salvo Lucía, que no tiene alternativa por compliance. Los motivos que dan:

- Se traba con 11 a 14 personas: Tomás, Javier, Sofía y Ricardo.
- No tiene votación: Tomás, Javier y Lucía.
- Agrupar notas es lento: Lucía y Ricardo.
- No tiene plantillas: Tomás y Javier.
- Cuesta encontrarla o no se sabía que existía: Lucía y Valeria.

**Implicación:** antes de agregar funciones al lienzo, el artefacto de la reunión tiene que vivir en la serie, el equipo o el canal, y no en la instancia de la reunión. Es la condición para competir con Miro, y también es condición del insight 1: no se puede retomar una decisión que no se encuentra.

> Evidencia: *"A las dos semanas, para la retro siguiente, fui a buscarla y no estaba. Quedó colgada del chat de esa reunión, y justo en el medio se había recreado la serie… Perdí los acuerdos, así de simple. Ahí dije: listo, volvemos a Miro."* (Tomás Aguirre)
>
> *"Desde entonces hago captura de pantalla al terminar y la pego en Confluence… Es cutre, pero es lo único que sé que voy a encontrar."* (Lucía Fernández)

## 4. Dentro de la empresa, el costo no son los minutos: es la gente que dicta, mira o no opina

Esto explica el dato de la encuesta según el cual el 46% de las reuniones internas deja a alguien afuera.

- **Quién queda afuera (6 de 10)** y por qué. Son causas internas, no de externos:
  - Licencias o instancias distintas según la filial: los de Lyon y México (Javier) y tres invitados sin licencia (Tomás).
  - Cuenta personal de Google logueada en el navegador: Valeria.
  - Falta de permiso en Confluence: Karla, en el caso de Sofía.
  - Laptops de 13 pulgadas o una sola pantalla: Lucía y Javier.
- **El patrón que resulta: dictarle al que tiene el mouse (6 de 10).** Pasa con Tomás, Javier, Lucía, Andrés, Martina y Diego. Para decir dónde mirar, *"nadie puede señalar"* (4 de 10: Tomás, Andrés, Diego y Valeria), y eso termina en errores reales. Andrés cerró el ticket equivocado y al cliente le llegó la notificación de cierre.
- **Lo que cuesta:** las objeciones no llegan a la reunión. Gloria no pudo entrar al FigJam y su desacuerdo con la decisión principal apareció una semana después, en un café. Los que menos hablan también son los recién llegados, los juniors y quienes están en otro huso horario (Andrés, Martina, Sofía y Ricardo).

**Implicación:** en las reuniones internas, el problema no es el tiempo de acceso sino la participación. Se necesita que cualquiera pueda señalar o marcar sobre lo que se comparte, sin tener cuenta ni licencia en la herramienta de origen, y que quien no entró pueda igual aportar su voto u objeción. El acceso de externos sigue siendo real (la agencia de Valeria, *"un infierno de permisos"*), pero ocurre *"una vez al mes"*.

> Evidencia: *"La gente que no entra al tablero no es poca. En casi todas hay alguien mirando desde afuera, y esa gente no opina. Eso me preocupa más que los minutos."* (Valeria Castro)
>
> *"Todo el mundo habla del acceso. Vale, el acceso es un problema al principio. Pero perder el hilo cada vez que cambias de herramienta es durante las dos horas."* (Javier Molina)

## 5. En las reuniones grandes, votar no decide: decide el líder cuando se acaba el tiempo, o la decisión se toma después entre pocos

**Recurrencia: 6 de 10** decidieron ellos mismos cuando se trabó la discusión o se acabó la hora (Tomás, Andrés, Lucía, Javier, Martina y Sofía). Tres no están seguros de que el grupo estuviera de acuerdo (Andrés, Martina y Sofía). Los votos que se usan hoy no generan confianza:

- Reacciones o manos contadas a ojo, con la mitad sin cámara: Andrés, Lucía y Ricardo.
- Votos dobles en FigJam, que terminaron en diez minutos discutiendo si el resultado valía: Valeria.

Incluso donde la votación funciona, solo ordena: *"Slido nos da un orden, pero la votación no decide"* (Javier). Dos entrevistados (Paula y Ricardo) sacaron las decisiones de la reunión grande a propósito y las toman entre 3 o 4 personas. Paula lo dice claro: votar con 20 personas es *"dar la sensación de que todos participaron"*.

**Implicación:** una función de votación sola no resuelve el problema. Lo que falta es un cierre explícito: una propuesta visible, el desacuerdo a la vista y la decisión registrada con quién la tomó. Eso vale también cuando decide el líder, que es el caso más común. Un voto anónimo y bien contado ayuda a que *"no gane el que más habla"* (Javier), pero es una pieza del cierre, no la solución.

> Evidencia: *"Hablamos veinte minutos. Al final decidí yo. Y dos devs se quedaron con cara de no, se notaba en la cámara."* (Martina Rojas)
>
> *"Las decisiones de verdad se toman en reuniones chicas, de tres o cuatro… A mí no me parece que eso sea decidir. Es dar la sensación de que todos participaron."* (Paula Benítez)

## Qué se repite entre entrevistas y con la encuesta

| Tema | Entrevistas (n de 10) | Encuesta |
|---|---|---|
| Decisión perdida con un costo concreto | 10 | 24% sin registro (Q9); registro y seguimiento: tema 1 de las abiertas (20%) |
| El líder transcribe el registro a mano | 8 | Aparece en las abiertas (R-124, R-050) |
| El resumen de IA falla como acta | 6 de 6 usuarios | 13 de 26 quejas en Q9 |
| Artefacto nativo perdido después de la reunión | 5 | 5 menciones en Q11 |
| Whiteboard probada y abandonada | 4 de 5 que la probaron | 43% la usó y la dejó (Q10) |
| Alguien dicta o mira sin participar | 6 | 46% de reuniones internas con alguien afuera (Q7) |
| El líder decide cuando se acaba el tiempo | 6 | Converger y votar: 15% de las abiertas |
| El artefacto vive afuera y no se quiere otra herramienta (Jira, Power BI, Confluence, Excel) | 4 (Martina, Diego, Sofía, Andrés) | 74% ya existía entre los no tableros (Q4) |

**Señales sin recurrencia:**

- **Compliance:** solo Lucía (España) no puede usar herramientas externas. Para ella *"lo nativo es lo único que tengo"* y el correo es lo que revisa auditoría. En la encuesta aparecía en 5 respuestas. Sigue siendo direccional.
- **El costo de saltar entre ventanas durante toda la reunión:** solo Javier.
- **"Demasiadas reuniones"** como dolor principal: solo Ricardo, y queda fuera del alcance de esta oportunidad.

## Preguntas que quedan abiertas

- ¿Cuántas cuentas del segmento pierden artefactos por recrear o reprogramar una serie? Se puede medir con telemetría: pizarras y notas huérfanas después de un cambio de invitación.
- ¿Confiarían en un resumen que muestre las decisiones para confirmar antes de cerrar la reunión, o igual lo revisarían después? Es la primera hipótesis a probar con un prototipo.
- Las entrevistas no cubren a quien *vive* en tableros visuales con grupos grandes. Tres entrevistados ofrecieron presentar a uno: Gonzalo Ferreyra (Paula), Daniela (Ricardo) y Carla, que hace retros sin tablero (Tomás).
