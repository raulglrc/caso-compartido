---
source: secondary
method: mixed
date: 2026-09-16
question: ¿Qué ofrecen Miro, Mural, FigJam, Zoom y Google Meet en acceso de invitados externos sin cuenta corporativa y en colaboración visual en vivo dentro de la reunión, y qué tan lejos o cerca está Teams de alcanzar paridad con eso dentro de sus restricciones de tiempo real y rendimiento antes de CollabCon?
opportunity: colaboracion-viva-en-reunion
---

# Research: colaboración visual en vivo — Miro, Mural, FigJam, Zoom y Google Meet

Los tres hallazgos que más deberían mover la conversación: (1) las tres herramientas dedicadas (Miro, Mural, FigJam) ya resolvieron el acceso de invitados externos sin cuenta corporativa como una función explícita y nombrada — no es un edge case sin resolver en el mercado, es tabla de apuestas; (2) la co-edición en vivo a escala de reunión **sí es técnicamente alcanzable dentro de una videollamada** — Zoom lo prueba con su propio Whiteboard nativo — así que la restricción de tiempo real/rendimiento del brief no parece ser el obstáculo real; pero (3) incluso Zoom, con feature nativo y sin fricción de "salir de la llamada", no ha cerrado la brecha de adopción/calidad frente a Miro (18x menos reseñas en G2, bugs de sincronización reportados, usuarios pidiendo "volver a Miro") — y Google, el otro gigante de colaboración, ni siquiera intentó construir un reemplazo propio de Jamboard: subcontrató la pizarra en vivo a Miro/FigJam/Lucidspark vía integración. Esto sugiere que el problema de Teams no es solo "construir la función" sino "construir la función Y ganar el hábito/confianza que hoy tiene un especialista con años de ventaja" — y que integrar (como hizo Google) puede ser una opción tan válida como reconstruir internamente.

Nota de alcance: esta corrida se limitó a dos preguntas (acceso de invitados y colaboración en vivo dentro de la llamada); el usuario dejó fuera, para esta ronda, precio/presupuesto en competencia directa y tendencia de mercado — donde aparecieron cifras de precio de forma incidental (no buscadas a propósito), se marcan como tales.

## Herramientas dedicadas: Miro, Mural, FigJam

| | Miro | Mural | FigJam |
|---|---|---|---|
| Acceso sin cuenta | **Visitor**: sin cuenta, puede ver/votar/videochat; edición solo si el equipo activa "Visitor editing" (desde plan Starter) [verificado: help.miro.com] | **Visitor**: ilimitados, solo lectura en plan Free; edición de invitados descrita en planes Business/Enterprise [verificado: mural.co/pricing] | **Open Sessions**: cualquiera edita sin cuenta ni login; la sesión expira a las 24h [verificado: figma.com/blog/introducing-open-sessions] |
| App nativa en Teams | Sí, pestaña embebida en reunión/canal/chat [verificado: help.miro.com] | Sí, "MURAL for Microsoft Teams" en Marketplace [verificado: mural.co] | Sí; FigJam **totalmente editable** dentro de Teams, Figma Design solo vista [verificado: help.figma.com] |
| App nativa en Zoom | No confirmada directamente (sí hay integración con Teams) | Sí, canvas embebido en la reunión de Zoom [verificado: mural.co/integrations/zoom] | Sí, crear/editar FigJam dentro de la reunión de Zoom [verificado: figma.com/product-integrations/zoom] |
| Precio (SaaS por asiento, aparte de M365) | Free $0 (3 boards) / Starter $8 / Business $20 por miembro/mes [verificado: miro.com/pricing] | Free $0 / Team+ $9.99–12 / Business $17.99 por mes [verificado: mural.co/pricing] | Unificado con Figma Design; cifras oficiales actuales no confirmadas en fetch — referencia de terceros: Collab seat ~$3–5, Full seat ~$16–90/mes [conocimiento del modelo / fuente agregadora — verificar] |
| Postura vs. Teams | Se compara frontalmente: "Microsoft Whiteboard ofrece funcionalidad básica" [verificado: miro.com/compare/miro-vs-microsoft-whiteboard] | Se posiciona como complemento de Teams, no como reemplazo ("Good for teams, great with Teams") [verificado: mural.co] | Mensaje de "sin login, sin fricción", no compara frontalmente contra Teams [verificado: figma.com/blog] |

**Lo que esto prueba:** el mercado ya trató "invitado externo sin cuenta no puede entrar a colaborar" como un problema de producto que se resuelve explícitamente — los tres tienen un mecanismo dedicado y nombrado para eso. **Lo que no prueba:** que el segmento de Camila cambiaría de herramienta solo por esto — los tres cobran SaaS por asiento separado de M365 (~US$8–20/usuario/mes en el caso de Miro y Mural), así que la pregunta de fondo sigue siendo si el dolor justifica pagar aparte o si alcanza con que Teams iguale la función gratis dentro de la licencia ya pagada.

## Zoom: colaboración nativa dentro de la propia videollamada

- **Zoom Whiteboard es nativo** (no integración de terceros) y permite co-edición simultánea sin límite fijo de editores, aunque con throttling bajo carga (con 100 participantes, solo ~30 pueden editar a la vez) [verificado: support.zoom.com KB0058148].
- En Gartner Peer Insights, Zoom Whiteboard (4.4/5, 173 reseñas) queda en el mismo rango que Miro (4.5), Lucid (4.5) y FigJam (4.6) — no destaca [verificado: gartner.com/reviews]. En G2, Zoom Workplace tiene mejor *score* que Miro en la categoría whiteboard (8.5 vs 8.1) pero con **18 veces menos reseñas** (400 vs 7.295) — consistente con muchísimo menor uso real de la función, no con mejor calidad [verificado: g2.com/compare/miro-vs-zoom-workplace].
- Reportes de bugs de sincronización y pérdida de formato en el foro de Zoom llevaron a al menos un usuario a plantear públicamente "volver a Miro" [verificado: community.zoom.com].
- **Acceso de invitados sin cuenta Zoom sigue incompleto**: un PM de Zoom confirmó en julio 2024 que el acceso sin cuenta "viene pronto"; para octubre 2024 y discusiones de 2025 seguía sin funcionar en casos embebidos [verificado: devforum.zoom.us]. Es decir, ni el competidor con feature nativo resolvió esto del todo, años después.
- **Zoom Docs / Canvas**: documento co-editable en vivo integrado a la reunión, incluido en licencias pagas de Zoom Workplace (sin SKU separado) [verificado: zoom.com/en/products/collaborative-docs].
- **Polls con "Rank Order"**: existe la función de priorización, pero usuarios la reportan rota (permite elegir la misma opción varias veces) desde 2021 hasta 2025 — no hay tablero visual de votación tipo post-its [verificado: community.zoom.com].
- Pricing: Basic gratis con 3 whiteboards; Business (~US$18–22/usuario/mes) agrega whiteboards ilimitados [verificado: fuente agregadora tldv.io — no confirmado directamente en zoom.com, que devolvió error al buscar el desglose].

**Lo que esto prueba:** la restricción de tiempo real/rendimiento del brief **no es un bloqueo técnico duro** — Zoom demuestra que se puede tener co-edición en vivo nativa dentro de una videollamada. **Lo que no prueba:** que construirlo cierre la brecha de adopción — Zoom lo construyó y aun así queda estructuralmente por detrás de Miro en engagement, con quejas de calidad y una función de invitados sin cuenta que sigue incompleta años después del anuncio.

## Google Meet: ni siquiera construyó una propia

- Google retiró Jamboard (app y hardware) entre octubre y diciembre de 2024 y **no construyó un reemplazo first-party** — integró Miro, FigJam y Lucidspark como apps de terceros dentro del panel de "Actividades" de Meet [verificado: workspaceupdates.googleblog.com 2023; workspace.google.com/blog — anuncio de la integración con Miro]. El propio anuncio de Google describe a Miro como "a third-party online collaborative whiteboarding app" — no como sustituto de Jamboard, sino como parche vía ecosistema.
- La co-edición de Docs/Sheets/Slides durante una llamada **sí es nativa**, pero con arquitectura inversa a lo que necesita Teams: el documento vive en su propia pestaña con Meet incrustado al costado, no la reunión con el documento incrustado [verificado: support.google.com/meet/answer/10540294].
- Encuestas nativas: solo opción única, sin ranking, resultados ocultos por defecto, y **ausentes en el plan de entrada** (Business Starter) [verificado: support.google.com/meet].
- Google sí ha invertido en abrir el acceso de invitados sin cuenta (incluida la posibilidad de participar en un tablero de Miro embebido sin perfil), lo que confirma que el acceso abierto es técnicamente viable a nivel de plataforma de videollamada, más allá de la herramienta de colaboración específica [verificado: workspaceupdates.googleblog.com 2024; help.miro.com].

**Lo que esto prueba:** ni el otro gran jugador de colaboración (Google) apostó a reconstruir la pizarra internamente — eligió integrar con el especialista. Es una señal de que "construir vs. integrar con Miro/FigJam" es una decisión estratégica legítima, no solo una salida de segunda categoría.

## Impacto en creencias

| Creencia (de overview.md / brief) | Veredicto | Evidencia |
|---|---|---|
| [opportunity: colaboracion-viva-en-reunion] [value] #3 — Team Leads necesitan colaboración visual en vivo con fuerza suficiente para pedirlo y rodear la limitación, y la alternativa nativa (Whiteboard) no los sostiene | **Apoya (parcialmente, por analogía de mercado)** | El patrón "alternativa nativa no sostiene" se repite en Zoom pese a tener whiteboard first-party sin fricción de salir de la llamada: 18x menos reseñas que Miro, bugs de sincronización, usuarios pidiendo volver a Miro. Es evidencia de mercado, no de los Team Leads del caso — no confirma la fuerza del pedido en este segmento específico, solo que el patrón no es exclusivo de Teams. |
| [product] [value] #1 — las organizaciones comparten links externos porque las herramientas nativas no cubren lo que necesitan (hoy solo correlación, no la razón) | **Matiza, no confirma ni contradice** | La evidencia de Zoom (nativo, sin fricción de salida, y aun así rezagado en engagement) sugiere que la causa puede no ser solo "falta de función" sino madurez/hábito/plantillas/confianza acumulada del especialista — una hipótesis alternativa a agregar a la lista, no una respuesta. Sigue sin poder confirmarse sin hablar con los Team Leads. |
| [opportunity: colaboracion-viva-en-reunion] [viability] #4 — resolver la sustitución mueve alguna métrica de negocio (upgrade, retención, ingreso/licencia) | **No dice nada** | Es investigación de mercado, no puede tocar una creencia sobre el efecto en las métricas internas de Teams — eso depende del cruce de datos propios ya listado en la agenda del brief. |
| [product] [viability] #6 — cuentas grandes pagarían el salto de US$8/usuario/mes de Premium a Max si las funciones resolvieran fricciones reales | **No dice nada (fuera de alcance esta ronda)** | El usuario excluyó la pregunta de precio/presupuesto de esta corrida. Dato incidental sin verificar a fondo: Miro Starter y Mural Team+ cobran en el mismo orden de magnitud (~US$8–12/usuario/mes) que ese salto de plan — coincidencia de rango, no evidencia de disposición a pagar. Pendiente si se decide research de precio dedicado. |

## Qué sigue necesitando research primario

Esta corrida solo tocó la pata de mercado de la agenda de investigación del brief (`/research-market`, ítem de viability). El resto de la agenda ya identificada en el brief sigue en pie, sin cambios por este hallazgo:

- **Datos que ya tiene el producto** (2-3 semanas, gratis): desagregar las 4.700 solicitudes y las sesiones de Whiteboard abandonadas en <2 min por motivo — este research de mercado no puede sustituir ese dato interno.
- **Encuesta** (`/design-survey`, 4-6 semanas): cuantificar si "invitado externo sin cuenta" es el motivo dominante de salir a Miro/Mural/FigJam frente a otras razones (falta de función, no lo encuentran, no confían en que otros puedan entrar) — esta corrida no puede decidir eso, solo confirmó que el mercado ya lo trata como un problema real y resoluble.
- **Entrevistas** (`/design-interview`, 6-8 semanas): confirmar o descartar la creencia de valor #3 con Team Leads del segmento, priorizando a quienes digan no tener el problema — la hipótesis alternativa que surge aquí (madurez/hábito del especialista, no solo función faltante) es justo el tipo de matiz que una entrevista puede resolver y una búsqueda web no.
- **Cruce de datos internos** (4-6 semanas): si el efecto dominante es retención o expansión — sin tocar por este research.

