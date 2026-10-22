# Evaluación · Complejidad de la fórmula AIQ para crear agentes

**Fecha:** 22 de octubre de 2026 · **Pedido por:** Oscar · **Tipo:** diagnóstico, sin cambios a los diseños.
**Fuentes revisadas:** `AgentMaker_Canon.md` (manda), `AIQ_Guia_Disenar_Agentes_v1.1.md`, `AIQ-AgentMaker-Fundamentos.md`, `AB02_Metodo_de_cursos.md`, kit `agente_d1_estratega_ia/`.

---

## 1. Veredicto

**Tu percepción es correcta, pero la causa no es la que parece.** Cada paso es fácil: el acelerador entrevista y la persona responde, y eso es de complejidad baja. Lo que sube la fórmula a **complejidad media (media-alta en el módulo 3)** es la cantidad: cuatro conteos distintos para lo mismo, 16 a 19 archivos, unas 48 operaciones manuales de copiar, adjuntar y descargar, y dos tareas de diseño propias de un profesional (el plano de ruta y el plan de pruebas).

Dicho simple: **lo difícil no es pensar, es administrar.** Y eso se puede quitar sin bajar la calidad, porque la calidad la pone el acelerador, no la cantidad de archivos.

---

## 2. Qué maneja el estudiante (módulo 3, Chief of Staff)

| Dimensión | Cantidad | Detalle |
|---|---|---|
| Conteos del mismo sistema | 4 | 6 piezas, 5 etapas CRAFT, 8 modos, unos 16 archivos. Ninguno coincide con otro |
| Conceptos nuevos | ~20 | Agente, proyecto, 6 piezas, acelerador, CRAFT (5 palabras en inglés), modo, tipo de ruta (estructurada, guiada, libre), matriz "qué saber / qué no hacer", contexto, conocimiento, expertise, guardrails, orquestador, documento por paso, plan de pruebas, change log, skill, `SKILL.md`, conector, rutina |
| Archivos que produce | 16 a 19 | Propósito, Plano de ruta, Contexto persona, Contexto negocio, Conocimiento de tema, Conocimiento experto, Guardrails, Instrucciones, 3 a 6 de pasos, Plan de pruebas, Change log, Guía de uso, `SKILL.md` |
| Operaciones manuales | ~48 | 6 acciones por modo (conversación nueva, pegar prompt, adjuntar los archivos correctos, responder, descargar, guardar) × 8 modos |
| Decisiones | 25 a 40 | Propósito, entregable, 3 o 4 criterios, insumos, tipo de ruta, 3 a 6 pasos, qué saber y qué no hacer en cada uno, aprobar cada archivo, 10 a 14 pruebas |
| Lecciones antes de usar el agente | 15 | El agente se usa de verdad recién en el módulo 4 |

**Kit de biblioteca (ejemplo D1 · Estratega de IA):** 16 archivos, 7 pasos de armado, 3 prompts de personalización recomendados, 10 casos de prueba. La guía promete "se arma en 3 minutos"; con este kit, subir los archivos sí cabe en minutos, pero llegar a "listo cuando" no `[SUPUESTO: sin cronometrar]`. Además, el kit D1 usa otra estructura (`D1_0x` y `KB0x`) que la de la guía (`1_Pega_esto`, `2_Arrastra_esto`, `3_Completa_esto`): el estudiante aprende dos formatos de kit.

---

## 3. Complejidad real contra complejidad percibida

| | Real (lo que hace) | Percibida (lo que ve) |
|---|---|---|
| Responder entrevistas | Baja. Habla como habla normalmente | Baja |
| Mover archivos entre conversaciones | Media. Es fácil equivocarse de adjunto o de versión | Media-alta. Se siente como "trámite" |
| Plano de ruta (Route) | Media-alta. Pensar el trabajo antes de delegarlo es la tarea más abstracta | Alta. Matriz, tipo de ruta y documentos que "nacen" de ella |
| Fix (10 a 14 pruebas y change log) | Media. Es práctica de ingeniería de software | Alta. Suena técnico para un líder |
| Takeoff (`SKILL.md`) | Baja con el acelerador | Media-alta. Un concepto nuevo justo antes de ver valor |
| Vocabulario (CRAFT, modos, piezas) | Nula: no cambia lo que hace | **Alta. Es la mayor fuente de percepción de complejidad** |
| Ensamblar un agente de la biblioteca | Baja-media | Media por la cantidad de archivos |

**Lectura:** la mayor parte de la complejidad percibida viene de cosas que no aportan a la calidad del agente: vocabulario, conteos que no coinciden y logística de archivos.

---

## 4. Comparación con un referente simple

El referente del video revisado en el otro hilo usa 3 piezas: un `agent.md` (cómo trabaja), archivos de contexto (qué sabe) y una skill (qué procedimiento repite). En un proyecto de Claude equivale a: instrucciones del proyecto + archivos del proyecto + skill.

| | Referente simple | Fórmula AIQ hoy |
|---|---|---|
| Piezas que la persona nombra | 3 | 6 piezas + 5 etapas + 8 modos |
| Archivos | 3 a 5 | 16 a 19 |
| Quién escribe | La persona (pantalla en blanco) | El acelerador entrevista (ventaja AIQ) |
| Calidad y confiabilidad | Depende de la persona | Alta: guardrails, pruebas, expertise con fuentes |

**Conclusión:** AIQ gana en calidad y en "nunca solo frente a la pantalla". Pierde en simplicidad visible. La meta es quedarse con la ventaja de AIQ y la cara del referente: **3 piezas visibles, 1 entrevista, el acelerador hace el resto.**

---

## 5. Simplificaciones de mayor impacto (propuesta; Oscar decide)

Ninguna cambia el diseño interno de los agentes ni su calidad. Cambian lo que el estudiante ve y mueve.

| # | Simplificación | Qué quita | Por qué no baja la calidad | Impacto |
|---|---|---|---|---|
| 1 | **Un solo modelo mental de 3 piezas para el estudiante:** Instrucciones (cómo trabaja), Archivos (qué sabe y qué respeta), Herramientas (conectores y skills). Las 6 piezas y los 8 modos quedan como mapa interno del acelerador | 3 de los 4 conteos; ~10 conceptos | El acelerador sigue produciendo las 6 piezas; solo cambia cómo se nombran ante el estudiante | Alto en percepción |
| 2 | **El acelerador como una conversación continua, no 8 prompts:** un proyecto de Claude "Acelerador" que conduce las etapas en orden y entrega un archivo al cierre de cada una | ~40 de las 48 operaciones manuales y el riesgo de adjuntar mal | Las etapas y sus puntos de aprobación se mantienen. `[DATO A VALIDAR]`: probar si una conversación larga pierde calidad; si pasa, un corte en Assemble | Alto en fricción real |
| 3 | **Consolidar a 5 archivos para el primer agente:** Instrucciones (incluye propósito y pasos), Contexto (persona y negocio), Conocimiento, Guardrails, Caso de prueba. Propósito y plano de ruta pasan a ser borradores internos de la entrevista | De 16-19 a 5 archivos | El contenido es el mismo, agrupado. La guía ya advierte que muchos documentos confunden a la IA; menos archivos con nombres claros también ayuda al agente | Alto en real y percibida |
| 4 | **Fix en 3 pruebas, no 10 a 14:** un caso normal, un dato faltante y un intento de romper un guardrail ("caza el error"). El plan completo y el change log, como nivel avanzado opcional | ~10 pruebas y un concepto técnico | Las 3 pruebas cubren los fallos más dañinos; quien quiere más, tiene el plan completo | Medio |
| 5 | **Valor antes de construir:** que el estudiante use un Chief of Staff listo en el módulo 2 (armado en minutos con el caso ficticio) y que CRAFT lo personalice con su contexto. Mover Takeoff (skill) al módulo 4, junto a su demostración | 15 lecciones sin usar el agente; un concepto antes de tiempo | Sigue construyendo cada pieza; solo cambia el orden. Encaja con "arrancar por lo que se va a producir" | Alto en motivación |

**Complementaria y barata:** unificar el formato de todos los kits de la biblioteca en `1_Pega_esto`, `2_Arrastra_esto`, `3_Completa_esto` (hoy D1 a D4 usan otra estructura), para que armar un agente se vea igual siempre.

---

## 6. Riesgos y documentos afectados si se adoptan

- **Riesgo de la 2:** conversación larga con pérdida de contexto. Se mitiga con un archivo al cierre de cada etapa y probándolo antes de grabar.
- **Riesgo de la 1:** CRAFT pierde visibilidad como marca. Puede seguir como nombre del acelerador, sin enseñar sus 5 palabras como contenido.
- **Documentos que habría que actualizar:** `AgentMaker_Canon.md` (secciones 2, 4 y 5), `AB02_Metodo_de_cursos.md` (secciones 2, 3 y 6), `AIQ_Guia_Disenar_Agentes_v1.1.md` (secciones 5 y 9), `AIQ-AgentMaker-Fundamentos.md` (secciones 5 y 8) y los kits D1 a D4 si se unifica el formato.

## 7. Siguiente paso sugerido

Cronometrar con 2 o 3 líderes reales el módulo 3 actual, contando dónde se atoran. Es la forma de convertir este diagnóstico, hoy `[HIPÓTESIS]`, en dato.

---

## 8. Actualización del 22 de octubre de 2026: implicaciones del nuevo temario

**Cambios que se tomaron en cuenta:** los 5 hitos del temario son las etapas CRAFT (Clarifica, Ruta, Arma, F, T). Cada persona elige su propio agente en Clarifica. La audiencia son líderes de negocio ambiciosos. El Hero es saber crear sus propios agentes Claude con un paso a paso claro y los riesgos bajo control. El Canon y AB02 quedan en revisión. Fuentes: `cursos/Transformacion_Zero_Hero_v1.md` y `cursos/Syllabus_AgentMaker_v2.md`.

**Efecto en el veredicto:** el nuevo temario resuelve parte de la complejidad percibida, porque ahora el estudiante ve una sola columna: 5 pasos que avanzan de cero a su agente. La complejidad real sigue siendo media. Los archivos, las operaciones manuales y los 8 modos no cambian, y aparece una carga nueva: como cada persona elige su propio agente, ya no puede copiar la ruta de un ejemplo común.

| # | Propuesta original | Estado con el nuevo temario | Ajuste |
|---|---|---|---|
| 1 | Mostrar solo 3 piezas | **Sigue vigente y se refuerza.** CRAFT pasa a ser lo visible, así que lo que sobra son las 6 piezas y los 8 modos | El estudiante ve **5 pasos y 3 piezas**. Los modos del acelerador se alinean con los hitos: 5 en lugar de 8 (Assemble deja de verse como 4 modos) |
| 2 | Acelerador como una sola conversación | **Cambia.** Con un hito por módulo, el corte natural es una conversación por hito | 5 conversaciones, una por hito, cada una cerrando con su archivo. Las operaciones manuales bajan de ~48 a ~15 `[SUPUESTO]` y desaparece el riesgo de una conversación demasiado larga |
| 3 | Pasar a 5 archivos | **Sigue vigente.** Encaja con un agente que crece por versiones (v0.1 a v1.0) | Un archivo nuevo o ampliado por hito. El syllabus v2 ya llega a "los 5 archivos" en Arma |
| 4 | Fix con 3 pruebas | **Se ajusta.** Probar es ahora parte del Hero ("riesgos bajo control") y un argumento de venta, no un trámite | F queda como hito completo, pero con mecánica simple: 3 pruebas guiadas (caso normal, dato faltante, intento de romper una regla) más un periodo de uso real. El change log y el plan de 10 a 14 pruebas quedan como material de referencia, no como tarea |
| 5 | Valor antes de construir | **Resuelto en buena parte.** El syllabus v2 tiene un agente v0.1 funcionando desde el módulo 1 | Falta decidir la skill: con T = "Termina y ponlo a trabajar", la skill puede ir en T o pasar a la biblioteca. Hay que evitar que sea un concepto nuevo justo al cierre |

**Carga nueva que trae la personalización:** el paso más abstracto es Ruta, y ahora cada persona diseña la ruta de su propio agente. Para que no sea una pantalla en blanco, hacen falta tres apoyos:
1. Un caso resuelto completo (el Chief of Staff ficticio) que se muestra en cada hito como modelo, aunque el estudiante construya otro agente.
2. Una galería corta de 4 o 5 rutas tipo (por ejemplo: analizar y decidir, preparar una conversación clave, diseñar un plan, revisar contra criterios), para que elija una y la adapte.
3. El filtro de alto AIQ en Clarifica, con 3 o 4 tareas sugeridas por función, para quien llega diciendo "quiero aprender IA".

**Biblioteca (módulo 5):** pierde peso como núcleo, porque el Hero es saber crear agentes y no recibirlos. La unificación de los kits sigue siendo útil, pero ya no es prioridad.

**Coherencia con la audiencia nueva:** para un líder ambicioso que paga por la guía, la complejidad visible pesa más que antes. Si el método se ve largo, contradice "un paso a paso claro". Las propuestas 1 y 2 son las que más protegen esa promesa.

**Documentos afectados:** la lista de la sección 6 queda sujeta a la revisión del Canon y AB02 que ya está abierta. Estas propuestas se pueden incorporar en esa misma revisión.
