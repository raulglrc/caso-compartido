---
source: synthetic
document: product/specs/2026-10-14-0219-recap-decisiones-confirmable.md
panel: joaquin-lemos (primary), beatriz-olmedo (primary), renata-schulz (tertiary)
date: 2026-10-14
---

# Panel de crítica: Resumen de decisiones confirmable

**Composición:** 2 primary (Joaquín Lemos, Beatriz Olmedo) y 1 tertiary (Renata Schulz). Se agregó a Renata porque la spec tiene implicaciones de permisos y de alcance.

**Procedencia:** `synthetic`. Es un ensayo con personas, no evidencia. Joaquín y Beatriz se derivan de entrevistas reales, pero lo que dicen aquí es una simulación. No se anota ninguna creencia de `product/overview.md` a partir de este panel.

---

### Joaquín Lemos — Engineering Manager que conduce retros y plannings · primary

**Valoración general:** 3/5

**Lo que me sirve:**
- La historia 3 es lo que más me importa. Si los acuerdos siguen en la serie cuando la recreamos, se resuelve el motivo por el que volví a Miro. *"¿Esto lo cumplimos?"* es lo primero que pregunto en cada retro.
- Me gusta que la lista se confirme con el grupo y no en mi versión. Cuando decido yo porque se acaba la hora, así al menos queda a la vista quién no estaba de acuerdo.
- Publicar en el canal con un clic reemplaza lo que hoy hago a mano en el hilo.

**Lo que me preocupa:**
- Lo que más tiempo me lleva no es reescribir el recap: es pasar cada acuerdo a Jira, de 20 minutos a una hora. La spec deja eso como está. Me ahorra la mitad del trabajo, no el trabajo.
- Mis decisiones se toman votando en el tablero. Si la lista solo capta lo que se dice, tengo que acordarme de decir en voz alta cada cosa votada, y eso es otra tarea para mí justo cuando no me sobra la cabeza (supuesto #19).
- Los últimos minutos son justo cuando ya no hay tiempo. Si la lista aparece cuando la reunión ya terminó, la gente se va y confirmo solo. Entonces es otra vez mi versión.
- La lista no guarda el enlace al frame del tablero, y sin él el acuerdo pierde contexto.

**Sugerencias:**
- Que la lista aparezca sola unos minutos antes del final programado, no cuando yo me acuerde de abrirla.
- Poder pegar en cada decisión un enlace al artefacto (el frame de Miro, el ticket).
- Aunque no haya integración con Jira, que se pueda copiar cada decisión como texto listo para pegar en un ticket: título, responsable, fecha y motivo.
- En la reunión siguiente, mostrar los acuerdos anteriores con una marca de "cumplido / no cumplido".

Si los acuerdos sobreviven a la serie, me pruebo esto en la retro sin pensarlo. Pero mientras siga copiando a Jira a mano, Miro no lo dejo.

---

### Beatriz Olmedo — Engineering Manager / Head de Operaciones, maneja el sistema en vivo · primary

**Valoración general:** 2/5

**Lo que me sirve:**
- Que la lista tenga **motivo**. El qué ya queda en Jira; lo que se me pierde es el porqué. Si eso queda escrito, me salva de reabrir discusiones un mes después.
- Que separe lo decidido de lo conversado. Es exactamente por lo que dejé el resumen de IA.
- Que "sin responsable" aparezca como vacío y no inventado. Lo que nos costó cuatro días con un cliente fue justamente que cada uno entendió que lo hacía el otro.

**Lo que me preocupa:**
- No llega al ticket. Yo dije que no quería otra herramienta ni otro lugar, y esto es otro lugar: la serie y el canal. Después igual tengo que pasar el porqué a Jira. Doble trabajo.
- Yo soy la que comparte pantalla con Jira y la que actualiza mientras me dictan. ¿Ahora además tengo que cambiar de pantalla para mostrar la lista y confirmarla? No veo cómo encaja con mi manera de conducir.
- La IA no ve lo que estaba en pantalla. Si decidimos "ese ticket" o "ese pico del gráfico", la decisión va a quedar sin el qué concreto.
- El canal no garantiza que lo lea quien tiene que ejecutar. El recap lo leyeron en México y lo entendieron mal; el problema no fue el lugar.
- Sinceramente, una parte de esto es disciplina. No estoy segura de que me haga falta una función.

**Sugerencias:**
- Como mínimo, que pueda mandar el motivo y el enlace al registro al ticket que se estaba mirando, aunque sea a mano con un clic.
- Que la lista se pueda abrir en un panel lateral sin dejar de compartir la pantalla de Jira.
- Que el responsable sea siempre una persona con nombre, no un equipo ni "Ecuador".
- Que quien es responsable de algo reciba aviso directo y no tenga que encontrarlo en el canal (lo que prueba B1).

Me gusta la idea del motivo, pero esta versión me resuelve un problema que no es el mío. Si no llega al ticket, sigo con mi correo.

---

### Renata Schulz — IT Manager / administradora de Microsoft 365 · tertiary

**Valoración general:** 3/5

**Lo que me sirve:**
- Que el registro quede dentro de Microsoft 365. No es otro proveedor, no tengo que pasar por Seguridad ni por el DPO.
- Si los equipos dejan de usar Miro para guardar acuerdos, es una licencia externa menos que justificar.

**Lo que me preocupa:**
- No dice en qué plan está. ¿Viene en Premium o es de Max? Si es de Max, necesito poder mostrar cuánto se usa antes de pedirle a Finanzas USD 8 por usuario.
- Depende de la transcripción. Si en algunas áreas la tenemos desactivada por política o por consentimiento, ¿qué pasa? ¿Funciona igual o la lista no aparece?
- ¿Dónde se guarda y cuánto tiempo? Necesito que siga las políticas de retención y de eDiscovery que ya tengo. Un registro de decisiones es justo lo que Auditoría va a querer revisar.
- Publicar en el canal: hay canales con invitados externos. No quiero que una decisión interna termine a la vista de un proveedor.
- No veo ningún control para mí: ni activarlo por área ni ver cuánto se usa.

**Sugerencias:**
- Definir el plan y agregar un reporte de uso en el Admin Center: reuniones con registro confirmado, por área.
- Aclarar qué pasa sin transcripción y respetar las políticas de retención existentes.
- Avisar o bloquear antes de publicar en un canal con invitados externos.
- Un interruptor de administración para activarlo por grupo.

A mí no me importa cómo se cierra una reunión, me importa poder justificarlo. Si viene con datos de uso y respeta mis políticas, no lo freno.

---

## Síntesis del panel

*Escrita como investigador, fuera del personaje.*

### En qué coinciden

- **La estructura con motivo y responsable explícito vale.** Joaquín y Beatriz valoran el motivo y que el campo vacío no se invente. Coincide con las causas reales de pérdida: responsable ambiguo (Andrés, Lucía) y porqué escondido (Martina, Sofía).
- **El valor queda a medias sin el paso al sistema de trabajo.** Los dos primarios dicen, por caminos distintos, que la parte más cara (pasar a Jira) sigue siendo manual. Esto pone presión directa sobre el supuesto #17. Es la consecuencia de la decisión de alcance del 2026-10-14.
- **La spec da por hecho que la IA capta todo lo que importa, y no es así.** Joaquín (votos en el tablero) y Beatriz (lo que está en pantalla) señalan el mismo hueco: la lista solo ve lo que se dice. Ya estaba registrado como #19 para el tablero; lo de la pantalla compartida no.

### Tensiones de diseño

- **Joaquín y Beatriz vs. el alcance:** los dos piden llegar al ticket o al artefacto (enlace, copia, envío), y el alcance decidido lo excluye. Hay que elegir entre mantener el recorte y probar #17 antes de construir, o reabrir una salida mínima a Jira.
- **Joaquín vs. Renata:** Joaquín quiere enlazar el registro con Miro; Renata quiere que todo quede dentro de Microsoft 365. Un enlace no saca datos, pero en cuentas con compliance (Agnieszka) puede chocar con la política.
- **Cuándo se confirma:** para que la confirmación sea del grupo, la lista tiene que aparecer *antes* de que se acabe el tiempo. Pero el patrón observado (6 de 10) es que el líder decide justo cuando se acaba la hora. Es un riesgo directo para el supuesto #18.

### Los cambios de mayor impacto

1. **Revisar la exclusión de Jira o probar #17 antes de construir.** Una salida mínima (copiar la decisión con motivo y responsable lista para pegar, o adjuntar el enlace al registro en el ticket que se compartió) atendería a los dos primarios sin una integración completa.
2. **Agregar un requisito de administración y viabilidad:** plan (Premium o Max), comportamiento sin transcripción, retención y eDiscovery, aviso en canales con invitados externos y reporte de uso. Hoy no hay ni una historia ni un supuesto que lo cubra, y es lo que pide quien decide la compra.
3. **Diseñar el momento de cierre:** que la lista aparezca sola unos minutos antes del final programado y se pueda abrir sin dejar de compartir pantalla. Así la confirmación es del grupo y no del líder después de que todos se fueron.

Posibles supuestos nuevos que salen del panel (no registrados; requieren aprobación):
- [feature: recap-decisiones-confirmable] [usability] Cuando la decisión se refiere a lo que se está mostrando en pantalla, la lista conserva el qué concreto (qué ticket, qué gráfico) sin que el líder lo complete a mano.
- [feature: recap-decisiones-confirmable] [viability] Los administradores de Microsoft 365 del segmento habilitan la función cuando respeta las políticas de retención y transcripción existentes y viene con un reporte de uso.
