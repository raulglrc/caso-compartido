---
spec: product/specs/2026-10-14-0219-recap-decisiones-confirmable.md
feature: recap-decisiones-confirmable
mechanism: incremental (elegido por el usuario)
status: draft
date: 2026-10-14
---

# Plan de exposición: Resumen de decisiones confirmable

## Hipótesis (de la spec, textual)

Creemos que los Team Leads del segmento que conducen reuniones de serie con decisiones van a **publicar el registro confirmado sin edición sustantiva** en al menos el 60% de esas reuniones, porque confirmarlo con el grupo antes de cerrar les quita la reescritura de 10 a 60 minutos y el riesgo de registrar ideas como decisiones.

Estamos equivocados si, en las reuniones donde se generó la lista, el líder agrega, quita o cambia una decisión, un responsable, una fecha o un motivo **después de cerrar** en más del 40% de los casos, o si sigue escribiendo su propio registro aparte (correo, hilo, recap reescrito) en más de la mitad de las reuniones.

## Secuencia de creencias

1. **Los líderes reconocen la lista como lo que se decidió.** Si la lista no refleja lo decidido, confirmar, publicar y retomar no tienen sentido.
2. **El grupo confirma la lista dentro de la reunión, sin alargarla** (#18). Si no se confirma con el grupo, lo que se publica es otra vez la versión del líder.
3. **El registro confirmado se publica sin reescribirlo y reemplaza al registro propio del líder** (#8, #17). Es la hipótesis de la spec.
4. **Los líderes retoman los acuerdos en la reunión siguiente de la serie.** Solo tiene sentido si ya existen registros confirmados que retomar.

## Niveles

### Nivel 1 — Ver las decisiones propuestas

- **Qué se revela:** durante la reunión, el organizador puede abrir la lista de decisiones propuestas (qué, responsable, fecha, motivo), separada del resumen. Los campos vacíos se muestran como vacíos. Cada decisión tiene un botón "no es una decisión". También se revelan los controles de administración que son condición para exponer: habilitar por grupo, respetar retención y eDiscovery, y no ofrecer la lista si la transcripción está desactivada. **Quedan ocultos:** editar, confirmar, publicar, copiar para ticket y el registro en la serie.
- **Creencia:** los organizadores abren la lista antes de cerrar y la reconocen como lo que se decidió: casi nada de lo propuesto es una idea registrada como decisión.
- **Audiencia:** organizadores de reuniones de serie en las cuentas donde el administrador habilitó la función.
- **Duración:** 2 semanas.
- **Validación:** **Avanzar si** el organizador abre la lista antes del final en ≥50% de las reuniones de serie en que se ofrece, y se marcan como "no es una decisión" ≤20% de las decisiones propuestas. **Detenerse si** la abre en <25% de esas reuniones, o se marcan >35%: es el error que ya causó daño (Paula) y no se avanza a confirmar sobre esa base.

### Nivel 2 — Corregir y confirmar con el grupo

- **Qué se revela:** todo lo del Nivel 1, más editar, quitar y agregar decisiones; mostrar la lista a todos los participantes dentro de la reunión; confirmarla con registro de quién y a qué hora; y la marca "sin confirmar" si la reunión termina antes. **Quedan ocultos:** publicar en el canal, copiar para ticket y el registro en la serie.
- **Creencia:** el grupo confirma la lista dentro de la reunión sin alargarla (#18).
- **Audiencia:** la misma, organizadores de reuniones de serie con la función habilitada.
- **Duración:** 2 semanas.
- **Validación:** **Avanzar si** la lista se confirma dentro de la reunión en ≥70% de las reuniones en que se abrió, y esas reuniones no duran más de 3 minutos más que la mediana de su serie. **Detenerse si** se confirma dentro de la reunión en <40%, o la confirmación agrega más de 5 minutos: en ese caso hay que rediseñar el momento de cierre (mejora 3 del panel) antes de seguir.

### Nivel 3 — Publicar en el canal y llevar al ticket

- **Qué se revela:** todo lo anterior, más publicar en el canal en un paso (con aviso si el canal tiene invitados externos), "copiar para ticket" en cada decisión y el reporte de uso para el administrador. **Queda oculto:** el registro en la serie y su retoma en la reunión siguiente.
- **Creencia:** los líderes publican el registro confirmado sin reescribirlo y dejan de escribir su propio registro aparte (la hipótesis de la spec, #8 y #17).
- **Audiencia:** la misma.
- **Duración:** 3 semanas.
- **Validación:** **Avanzar si** ≥60% de los registros confirmados se publican sin edición sustantiva posterior al cierre, y en una muestra de líderes consultados, menos de la mitad sigue escribiendo su propio registro aparte. **Detenerse si** hay edición sustantiva después del cierre en >40% de los registros, o más de la mitad de la muestra sigue con su correo, hilo o recap reescrito: la hipótesis no se sostiene y no se construye el retomar.

### Nivel 4 — Retomar los acuerdos en la serie

- **Qué se revela:** todo lo anterior, más los registros confirmados guardados en la serie y ordenados por fecha, que siguen apareciendo aunque la serie se reprograme o se recree, y un acceso al último registro al empezar la reunión siguiente.
- **Creencia:** los líderes retoman los acuerdos anteriores al empezar la reunión siguiente de la serie.
- **Audiencia:** la misma, con al menos un registro confirmado en su serie.
- **Duración:** 3 semanas (dos o más reuniones por serie).
- **Validación:** **Avanzar si** el organizador abre el registro anterior en ≥50% de las reuniones siguientes de series que tienen un registro confirmado. **Detenerse si** lo abre en <20%: el retomar no es motivo suficiente y la persistencia vuelve a evaluarse con la rama de tablero visual.

## Mecanismo de exposición

**Incremental, por elección del usuario: es vinculante.** Encaja en algo: los niveles son acumulativos y ninguno necesita un subgrupo por comportamiento distinto al de los otros. Pero hay tres límites:

- **La población entera.** Con incremental, cada nivel llega a toda la población de despliegue, y Teams Meetings está en producción con cientos de millones de usuarios. El único filtro que queda es el interruptor del administrador (historia 5), que controla el cliente y no el equipo.
- **Sin vuelta atrás.** Si un nivel falla en su "detenerse si", no hay forma de ocultarlo sin otro despliegue.
- **Contexto entre iteraciones.** Hay que confirmar con ingeniería que el agente que programa conserva el contexto de un nivel al siguiente.

La decisión final del mecanismo es de ingeniería.

## Validaciones en paralelo

- **Rentabilidad (#12, #4):** cruzar el uso sostenido del resumen de IA con la renovación y el upgrade a Max en el segmento. Decide si la función se presenta como motivo de upgrade.
- **Adopción por administradores (#21) y plan:** conversaciones con administradores de Microsoft 365 del segmento y con ventas/CSM, para decidir si la función va en Premium o en Max antes del Nivel 3, que trae el reporte de uso.
- **Factibilidad de la extracción (#9):** T2 con tech; su umbral de precisión (≥90%) es la precondición técnica del Nivel 1.
- **Persistencia en la serie (#20):** confirmar con tech, antes del Nivel 4, que el registro sobrevive a reprogramar o recrear la serie.
- **Compliance en el EEE:** verificar que transcripción, retención y publicación cumplen en las cuentas con restricciones (5 menciones, direccional).

## Preguntas abiertas para el equipo de producto

- T1 sigue sin correr. ¿Se corre T1 antes del Nivel 1? Es la forma más barata de saber si una lista bien hecha se publica sin reescribirla, antes de exponerla a toda la población.
- La telemetría ve las ediciones posteriores al cierre, pero no los correos ni los hilos de Slack que el líder escribe aparte. ¿Cómo se arma la muestra de líderes para medir el registro propio y la reducción de tiempo (#17)?
- Con incremental no se puede limitar la exposición al segmento (tech grande y distribuido). ¿Los umbrales se leen sobre toda la población o se filtra el análisis por segmento?
- Decisiones tomadas sobre un tablero externo (#19): ¿se mide aparte cuántas decisiones de reuniones con un enlace a Miro o FigJam faltan en la lista?
- Calendario: cuatro niveles suman unas 10 semanas más las de construcción. ¿Qué nivel tiene que estar visible para la exhibición en CollabCon (≈ mediados de febrero de 2027)?
