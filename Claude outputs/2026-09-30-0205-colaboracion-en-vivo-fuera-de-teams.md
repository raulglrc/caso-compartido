---
source: survey
survey_design: product/surveys/2026-09-23-1944-colaboracion-en-vivo-fuera-de-teams.md
results: product/surveys/2026-09-26-1800-respuestas-colaboracion-en-vivo-fuera-de-teams.csv
n: 210 completas (email 76, panel 134) — de ellas 182 trabajaron afuera y 28 no
date: 2026-09-30
---

# Análisis de encuesta: trabajo colaborativo fuera de Teams en reuniones de más de 5 participantes

## Denominador y límites

| | Email (organizadores del segmento) | Panel B2B | Total |
|---|---|---|---|
| Entradas | 85 | 164 | 249 |
| Descalificadas en el filtro | 8 (9%) | 26 (16%) | 34 |
| Parciales (excluidas) | 1 | 4 | 5 |
| **Completas** | **76** | **134** | **210** |
| Trabajaron en una herramienta externa (Q1 ≠ "En ninguna") | 65 | 117 | **182** |
| No trabajaron afuera (Q1 = "En ninguna") | 11 | 17 | **28** |

- **Campo:** del 23/09 12:39 al 25/09 09:39. Se cerró antes del 26/09 previsto.
- **Tasa de respuesta:** el panel completó 134 de una cuota de 150 (89%). La del email no se puede calcular: el alcance quedó `unknown` en el diseño y sigue sin confirmarse.
- **Metas:** ≥150 que trabajaron afuera, cumplida (182). ≥30 por canal, cumplida. ≥30 que no trabajaron afuera, **no cumplida (28)**: todo lo que se diga de ese grupo es **direccional**. El email tenía que aportar al menos 150 y aportó 76; la meta total se alcanzó gracias al panel.
- **Sesgos que heredan todas las cifras:**
  - El email es un canal propio y sobrerrepresenta a quienes siguen conformes con Teams. Se nota en los datos (ver "Diferencias entre canales").
  - En el panel, la firmografía (sector y países) es autodeclarada. En el email, sector y países no se preguntaron porque los garantiza la lista.
  - Las preguntas Q2 a Q9 se refieren a la última reunión y dependen del recuerdo de quien la condujo. Q6 y Q7 son estimaciones del organizador, que probablemente no ve a todos los que se quedaron afuera.
- **Calidad:** no hay filas duplicadas. Hay 4 completas por debajo de un tercio de la duración mediana (menos de 80 s frente a 233 s). Al excluir todas las de menos de 100 s (n = 195), las cifras centrales cambian menos de 2 puntos. Se mantienen en la muestra.
- **Nota de método:** en Q9 la opción "Otro" llegó al **17,6%**, por encima del umbral del 15% que fijó el diseño, así que la lista está incompleta. En 26 de esos 32 "Otro" la respuesta es "en el resumen o recap de IA, en la transcripción o en la grabación", una opción que faltaba. Q2, Q3 y Q5 quedaron por debajo del 5%.

## Diferencias entre canales (describen la muestra antes que el segmento)

| Indicador | Email | Panel |
|---|---|---|
| Trabajaron afuera en más de la mitad o en todas sus reuniones (Q1) | 21% | 40% |
| Hubo externos en la reunión (Q8) | 17% | 24% |
| Lo decidido quedó en el chat o las notas de Teams (Q9) | 23% | 7% |
| Usan las notas de Loop en algunas o en la mayoría de sus reuniones (Q10) | 37% | 22% |
| El artefacto ya existía antes de la reunión (Q4) | 43% | 59% |
| El artefacto se creó para la reunión y no se volvió a usar (Q4) | 23% | 11% |

Estas diferencias van en la dirección del sesgo que se anticipó: quienes llegan por el email salen menos de Teams y usan más lo nativo. Por eso las cifras de intensidad y de origen del artefacto se reportan por canal. Lo que coincide entre canales es lo más sólido: el orden de las actividades (Q5), el porcentaje de reuniones sin registro de lo decidido (Q9: 25% en email y 24% en panel), los participantes que no lograron entrar (Q7: 49% y 51%) y el tema principal de las respuestas abiertas.

## O1. Origen del artefacto

**Qué creíamos:** si el tablero o documento externo ya existía antes de la reunión, el problema es de integración con los sistemas donde vive el trabajo y no de colaboración en vivo.

**Qué muestran los datos** (base: los 182 que trabajaron afuera):

- En el **53%** de los casos el artefacto ya existía antes de la reunión (51% siguió usándose después y 3% no). En el 39% se creó para la reunión (24% siguió usándose y 15% no). El 7% no lo sabe.
- La cifra total esconde dos grupos distintos, que se separan según la herramienta (Q2 × Q4):

| Herramienta usada (Q2) | n | Ya existía | Se creó para la reunión |
|---|---|---|---|
| Solo otras herramientas: Docs, Jira, dashboards, Confluence, Notion… | 121 | **74%** | 18% |
| Al menos un tablero visual: Miro, Mural, FigJam o Lucidspark | 61 | 13% | **82%** (y 52% se siguió usando) |

- Las herramientas más citadas (Q2, opción múltiple) son Google Docs, Sheets o Slides (32%), Jira (29%), Miro (20%), dashboards (16%) y Confluence (14%). Los tableros visuales aparecen en el **34%** de las reuniones.

**Qué decisión se sigue:** con el criterio del diseño, el problema dominante es de **integración**: la mayor parte del trabajo externo ocurre sobre artefactos que ya viven en Jira, en Docs o en un dashboard. Hay además un subgrupo claro, un tercio de las reuniones, que crea tableros para la reunión y los sigue usando después. Ese subgrupo sí corresponde a la oportunidad tal como está formulada. Conviene tratarlos como dos problemas distintos y no como uno solo.

## O2. Costo de acceso

**Qué creíamos:** entrar a la herramienta cuesta 5 minutos o más, y hay que ver si esa fricción se concentra en las reuniones con externos.

**Qué muestran los datos:**

- **27%** tardó 5 minutos o más en que todos estuvieran dentro, y **46%** lo logró en menos de 2 minutos.
- La diferencia la marca la presencia de externos (Q6 × Q8):

| | Con externos (n = 39) | Sin externos (n = 137) |
|---|---|---|
| Tardaron 5 minutos o más | **62%** | 18% |
| Tardaron menos de 2 minutos | 13% | **57%** |
| Al menos 1 participante no logró entrar (Q7) | 64% | **46%** |

- Hubo externos en el 21% de las reuniones que trabajaron afuera.
- Q3: el 54% llegó a la herramienta por un enlace pegado en el chat, el 22% ya la tenía abierta antes, el 15% la abrió por su cuenta mientras alguien compartía pantalla y solo el **8%** la abrió como app dentro de la reunión. La telemetría de enlaces en el chat ve poco más de la mitad del fenómeno.

**Qué decisión se sigue:** para las reuniones internas, el umbral de 5 minutos **no se sostiene**. La fricción de tiempo se concentra en las reuniones con externos, que según el diseño corresponden a otro segmento (consultores y agencias). Queda abierta una pregunta dentro del segmento: aun sin externos, en casi la mitad de las reuniones alguien siguió mirando la pantalla de otro. Sin saber por qué, no se puede decidir (ver "Preguntas para entrevistas").

## O3. Qué se hace afuera y dónde queda la decisión

**Qué creíamos:** las opciones venían del trabajo de escritorio; la idea era ver qué actividad tendría que cubrir cualquier solución, incluida la IA.

**Qué muestran los datos:**

- **Actividades** (Q5, opción múltiple, n = 182): votar o priorizar 40%, editar un documento entre varios 35%, revisar datos y señalar algo puntual 34%, anotar decisiones o acuerdos 33%, aportar ideas 29%, actualizar tickets 25%, agrupar ideas 22%, diagramar 13%. Las actividades típicas de pizarra (aportar, agrupar, diagramar) no encabezan la lista. Encabezan las de **decidir y registrar**. El orden es igual en los dos canales.
- **Dónde quedó lo decidido** (Q9): no quedó registrado en ningún lado **24%**, en un chat fuera de Teams (Slack, WhatsApp) 23%, en Jira 23%, en la misma herramienta externa 15%, en el chat o las notas de Teams 13%, en un documento de actas 12%, en un correo 10%. Otro **14%** lo dejó en el resumen de IA, la transcripción o la grabación (la opción que faltaba), y **13 de esos 26** agregan una reserva sin que se les pregunte: *"no distingue lo decidido de lo conversado"*, *"con errores"*, *"que nadie leyó"*.
- **Respuestas abiertas** (Q11: 95 respuestas, 38 por email y 57 por panel), agrupadas en temas:

| Tema | Menciones | Evidencia |
|---|---|---|
| **Registro y seguimiento de lo decidido** (quién lo escribe, dónde queda, qué se cumple) | 19 | *"Termino escribiendo el acta yo después de cada reunión y pasando las tareas a Jira a mano. Es trabajo que nadie ve"* (R-124, panel) · *"Tuvimos un release que salió con el alcance viejo porque la decisión quedó en un comentario"* (R-144, panel) |
| **Continuidad entre reuniones y encontrar lo anterior** | 14 | *"Cada reunión es una isla. Lo que se trabajó en la anterior está en otro lado"* (R-166, panel) · *"Buscar el material de la reunión pasada me lleva más que la reunión"* (R-031, email) |
| Temas ajenos a la colaboración (demasiadas reuniones, husos horarios, idioma, audio, rendimiento) | 13 | *"Coordinar horarios entre 4 países"* (R-075) |
| Converger, priorizar, votar y cerrar | 12 | *"Divergir es fácil, todos tiran ideas. Ordenarlas y elegir es lo que nos cuesta"* (R-011, email) · *"Usamos reacciones en el chat pero nadie sabe cuántos votaron ni qué ganó"* (R-053, panel) |
| Participación desigual y atención | 11 | *"Hay 12 personas y opinan 3, el resto escucha o está en otra cosa"* (R-049, email) |
| Acceso a la herramienta externa (4 de las 11 menciones hablan de externos) | 11 | *"Los permisos del Miro. Siempre hay alguien que no puede editar y pierde los primeros 10 minutos"* (R-244, panel) |
| Limitaciones o poca visibilidad de lo nativo | 9 | *"El whiteboard no deja ordenar ni votar, es una hoja en blanco y ya"* (R-239, panel) |
| Compliance o regulación que limita las herramientas externas | 3 | *"Compliance no nos deja meter datos de clientes en Miro, así que o lo hacemos en Teams o no se hace. Y en Teams cuesta"* (R-190, email) |
| Sin problema o no aplica | 3 | *"No aplica, mis reuniones grandes son informativas"* (R-229) |

Los dos primeros temas forman lo que aquí se llama **la memoria de la decisión**: suman 33 de 95 respuestas (35%), aparecen en los dos canales (13 por email y 20 por panel) y también en el grupo que no trabaja afuera. Dentro de esos temas hay dos patrones más finos. Cinco personas cuentan que perdieron la pizarra de Teams de la reunión anterior (*"en Miro por lo menos el tablero tiene un link fijo"*, R-218). Tres dicen que el resumen de IA no separa lo que se decidió de lo que solo se conversó.

**Qué decisión se sigue:** cualquier solución tiene que cubrir la secuencia completa: **converger → decidir → registrar → retomar en la reunión siguiente**, y no solo un lienzo compartido. El lugar más claro para la IA es un resumen que separe las decisiones, con dueño y fecha, de lo que solo se conversó, y que las lleve adonde vive el trabajo (Jira, el tablero, la reunión siguiente). Esto se sostiene por igual en los dos canales.

## O4. Conocimiento y uso de lo nativo

**Qué creíamos:** había que separar "no me sirve" de "no sé que existe".

**Qué muestran los datos** (Q10, n = 210):

| Función | No sabía que existía | La conoce y nunca la usó | La usó y dejó de usarla | La usa |
|---|---|---|---|---|
| Whiteboard | 8% | 27% | **43%** | 21% |
| Notas de la reunión (Loop) | **31%** | 28% | 14% | 27% |
| Apps de otras herramientas dentro de la reunión | **40%** | 28% | 9% | 23% |
| Resumen o asistente de IA | 12% | **39%** | 13% | **36%** |

- **Whiteboard tiene un problema de "no me sirve":** la probó casi la mitad y la dejó. En las respuestas abiertas, los motivos son que no tiene votación ni agrupamiento, que le faltan plantillas, que se traba con más de 8 personas y, sobre todo, que no se encuentra en la reunión siguiente.
- **Las apps dentro de la reunión y las notas de Loop tienen un problema de "no sé que existe":** 40% y 31% no las conocían. Encaja con que solo el 8% abrió la herramienta externa como app dentro de la reunión.
- **La IA es la función nativa más adoptada (36%),** y aun así el 39% la conoce y nunca la usó.
- El grupo que no trabaja afuera (n = 28, direccional) no muestra más uso de lo nativo que el resto. En Q12 (16 respuestas) cuenta que decide con recursos improvisados: votos a mano alzada, con reacciones o con Forms (4), alguien comparte un Excel o una presentación y escribe lo que le dictan (3), se habla y alguien anota en el chat, en OneNote o por correo (3), compliance les prohíbe las herramientas externas (2), usan la pizarra o las notas de Teams (2). Hacen las mismas tareas que el resto, con peores medios. No es un grupo que "no lo necesite".

**Qué decisión se sigue:** Whiteboard necesita cambios de producto (persistencia a lo largo de una serie de reuniones, votación y agrupamiento, rendimiento). Las apps dentro de la reunión y las notas de Loop necesitan primero que se las conozca: es una palanca barata que conviene probar antes de construir algo nuevo.

## Insights

### 1. El problema dominante es la memoria de la decisión, no el lienzo visual

En una de cada cuatro reuniones que trabajaron afuera, lo decidido no quedó registrado en ningún lado (24%, igual en los dos canales). Otro 23% lo dejó en un chat fuera de Teams, y el 35% de las respuestas abiertas habla de registrar y retomar lo decidido. El resumen de IA ya ocupa ese lugar para el 14%, pero la mitad de ellos desconfía de lo que registra. Una solución que ayude a cerrar y registrar decisiones (quién, qué, para cuándo, por qué) y a retomarlas en la reunión siguiente responde a lo que más se repite en los datos.

> Evidencia: *"El resumen automático sirve para saber de qué se habló pero no para saber qué quedó decidido, lo tengo que corregir siempre"* (R-149, panel)

### 2. "Salir de Teams" son dos problemas distintos: artefactos que viven afuera y tableros creados para la reunión

El 74% de quienes usaron Docs, Jira o dashboards trabajó sobre algo que ya existía, lo que es un problema de integración. El 82% de quienes usaron Miro, Mural o FigJam creó el tablero para la reunión, lo que sí es colaboración en vivo, y eso ocurre en un tercio de las reuniones. La oportunidad está formulada como colaboración "visual" y solo cubre ese tercio. Conviene separarla en dos ramas del árbol de oportunidades antes de elegir una solución.

> Evidencia: *"Tenemos un tablero de Miro por trimestre y ahí va todo, es la única forma de no perder el hilo entre reuniones"* (R-249, panel)

### 3. Whiteboard se abandona por falta de funciones y porque se pierde después de la reunión

El 43% de los encuestados la probó y la dejó. Los motivos que mencionan son concretos: no permite votar ni agrupar, no tiene plantillas, se traba con muchas personas escribiendo a la vez y no se encuentra en la reunión siguiente. Esto último enlaza con el insight 1. Un tablero que no persiste a lo largo de una serie de reuniones pierde justamente frente a Miro, que ofrece un enlace fijo.

> Evidencia: *"Armé una retro en la whiteboard de Teams y a la semana siguiente no la pude encontrar para continuar. Volvimos a Miro"* (R-089, panel)

### 4. La fricción de acceso fuerte está en las reuniones con externos, pero en la mitad de las reuniones internas alguien se queda afuera

Tardar 5 minutos o más es la norma con externos (62%) y la excepción sin ellos (18%). Sin embargo, el 46% de las reuniones internas dejó al menos a una persona mirando la pantalla de otro. El acceso de invitados externos es un problema de otro segmento. Dentro del segmento, el problema es de participación: no es cuestión de tiempo, sino de que alguien no entra o no sabe usar la herramienta.

> Evidencia: *"Algunos no saben usar Miro y se quedan mirando. Pierdo gente en el camino"* (R-147, email)

### 5. Hay que empezar por dar a conocer lo que ya existe

El 40% no sabía que se pueden abrir apps de otras herramientas dentro de la reunión, y solo el 8% entró así. El 31% no conocía las notas de Loop. Antes de construir un lienzo nuevo, un experimento de visibilidad (proponer abrir como app el enlace que se pega en el chat) cuesta poco y mediría si la integración resuelve el problema del insight 2.

> Evidencia: *"No sabía que Teams tenía notas de reunión hasta que alguien las abrió de casualidad. Estaban ahí y nadie las usaba"* (R-040, email)

**Señal menor para vigilar:** compliance o regulación aparece 5 veces (3 en Q11 y 2 en Q12). En España el 19% no trabaja afuera, contra el 13% general (n = 27, direccional). En esas cuentas, lo nativo es la única opción y no una alternativa más.

## Preguntas para entrevistas (el porqué que la encuesta no responde)

1. ¿Por qué alguien se queda afuera en casi la mitad de las reuniones **internas**: permisos, SSO, no sabe usar la herramienta o prefiere mirar?
2. ¿Qué convierte algo en "decidido y registrado" para un Team Lead? ¿Por qué el resumen de IA no alcanza: le falta estructura, falla en precisión o nadie confía en él?
3. ¿Por qué lo decidido termina en Slack o WhatsApp (23%)?
4. Entre quienes dejaron Whiteboard, ¿qué pesó más: las funciones, la persistencia, el rendimiento o que los demás no entraban?
5. Con artefactos que ya existen (Jira, dashboards), ¿qué haría falta para trabajarlos dentro de la reunión? ¿Alcanza con abrirlos como app?
6. En cuentas con restricciones de compliance, ¿qué hacen hoy y qué necesitarían de lo nativo?

Diez personas del grupo de reclutamiento ya fueron entrevistadas entre el 25 y el 28/09 (ver abajo). Sus transcripciones pueden responder parte de estas preguntas antes de diseñar una ronda nueva.

## Grupo de reclutamiento (opt-in)

77 aceptaron una conversación. Son candidatos 64 (se excluyen 6 de IT y 7 que conducen como máximo una reunión por semana), y 6 de ellos no dejaron contacto. Hay 47 con al menos una señal que **contradice** la creencia: Q1 "En ninguna", Q4 "Ya existía…", o Q6 por debajo de 2 minutos. Los datos de contacto están en el CSV.

**Ya entrevistados (25 al 28/09):** Diego Paredes (R-036, Q4 + Q6), Martina Rojas (R-224, Q4 + Q6), Sofía Martínez (R-151, Q4 + Q6), Lucía Fernández (R-143, Q1), Ricardo Salinas (R-196, Q1), Andrés Quintero (R-170, Q1), Paula Benítez (R-153, Q1), Tomás Aguirre (R-113), Javier Molina (R-097) y Valeria Castro (R-024).

**Próximos candidatos, primero los que contradicen la creencia:**

| Prioridad | ID | Nombre | País | Contradice | Por qué conviene |
|---|---|---|---|---|---|
| 1 | R-120 | Irene Blanco | Colombia | Q1 ninguna | *"Las decisiones quedan en el aire… la grabación nadie la mira"* |
| 1 | R-046 | Mateo Gómez | Argentina | Q1 ninguna | Comparte un Excel y escribe lo que le dictan: *"si no lo anoto yo no lo anota nadie"* |
| 1 | R-009 | Jimena Paz | Colombia | Q1 ninguna | Compliance le prohíbe las herramientas externas: *"nadie quiere ser el que decide"* |
| 1 | R-085 · R-088 · R-242 · R-135 | Isabella Vargas · Ana Lozano · Rocío Figueroa · Álvaro Cano | CO · AR · MX · BR | Q1 ninguna | Completan el grupo que no trabaja afuera (n = 28, por debajo de la meta) |
| 2 | R-144 | Pilar Ruiz | Chile | Q4 + Q6 | Un release salió con el alcance viejo porque la decisión quedó en un comentario |
| 2 | R-235 | Felipe Acosta | Colombia | Q4 + Q6 | Facilita y opina a la vez |
| 2 | R-234 | Martín Espinoza | Chile | Q4 + Q6 | Con más de 8 personas se pisan |
| 2 | R-131 | Sara Molina | España | Q4 + Q6 | Sin propuesta escrita previa, la reunión da vueltas (cuenta del EEE) |
| 2 | R-102 · R-094 · R-240 · R-180 · R-176 · R-128 | Nicolás Castillo · Alejandro Navarro · Constanza Lagos · Agustín Ledesma · Emiliano Cabrera · Ignacio Arce | varios | Q4 + Q6 | Sin respuesta abierta: la conversación sería exploratoria |
| 3 | R-173 · R-090 | Josefina Palma · Luis Carrasco | España | Q6 | Normativa europea y priorización del backlog con pantalla compartida |
| 3 | R-065 · R-086 · R-244 | Carla Muñoz · Laura Gil · Gonzalo Reyes | EE. UU. · MX · PE | Q4 | Whiteboard que se pierde · "lo vemos por Slack" · permisos de Miro |

Hay dos candidatos con doble señal que respondieron demasiado rápido (R-057 en 79 s y R-247 en 83 s). Conviene verificarlos antes de invitarlos.
