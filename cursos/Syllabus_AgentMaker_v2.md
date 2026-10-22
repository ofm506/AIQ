# Syllabus · AIQ AgentMaker · Construye tu agente desde el módulo 1

**Versión:** 22 de octubre de 2026 · propuesta para decisión de Oscar.
**Cambia:** la secuencia estándar de `AB02_Metodo_de_cursos.md` §2 y la tabla de `AgentMaker_Canon.md` §5. Mantiene el 4+1, CRAFT, los 8 modos del acelerador, el Chief of Staff y la biblioteca del M5.
**Para quién:** líderes de negocio que no programan. Se aplica igual al curso de ventas cambiando el primer agente (Calificador de oportunidades) y el caso (Valeria Soto, Tracta, ficticio).

---

## 1. La idea en una frase

Tu agente funciona desde el módulo 1 y mejora en cada módulo.

En la versión anterior, quien tomaba el curso pasaba los módulos 1 y 2 entendiendo qué es un agente y empezaba a construir en el módulo 3. Ahora cada módulo termina con el agente funcionando en una versión mejor que la anterior. CRAFT deja de vivir solo en el módulo 3 y se reparte a lo largo del curso.

| Módulo | Etapa de CRAFT | Tu agente al terminar |
|---|---|---|
| 1 | Clarify | **v0.1 · Ya conversa contigo.** Sabe para qué existe, qué entrega y te entrevista antes de responder |
| 2 | Route | **v0.2 · Ya sigue tu método.** Trabaja por los pasos que tú definiste |
| 3 | Assemble | **v0.3 · Ya es experto.** Conoce tu realidad, aplica las mejores prácticas y respeta tus reglas |
| 4 | Fix + Takeoff | **v1.0 · Ya trabaja contigo.** Probado, corregido, con su skill y usado con un caso real |
| 5 | Biblioteca | **Tu equipo de agentes.** Agentes nuevos que arrancan con el contexto que ya construiste |

## 2. Reglas del curso (las que eliminan fricción)

1. **Primero haces, después entiendes.** Cada lección dura menos de 5 minutos `[SUPUESTO]` y solo explica lo que harás en la práctica siguiente.
2. **Nunca empiezas en blanco.** Cada práctica trae el prompt del acelerador listo para pegar y el ejemplo resuelto del caso ficticio al lado.
3. **Respondes, no redactas.** El acelerador te entrevista; tú contestas como hablas y revisas el archivo que produce.
4. **Un módulo, una versión del agente.** Al cerrar cada práctica pruebas tu agente con una situación real de tu semana.
5. **Todo vive en una carpeta.** Desde el módulo 1 tienes la carpeta del agente con nombres de archivo fijos; el montaje es revisar una lista.
6. **Se corrige el archivo, no el chat.** Lo que arreglas en una conversación se pierde; lo que arreglas en el documento queda.
7. **Alto AIQ siempre.** El agente se elige por una situación de negocio con su métrica, no por curiosidad.

## 3. El kit de arranque

Lo recibes antes de la lección 1.1, para que nada te detenga en la primera práctica.

| Pieza | Qué es | Estado |
|---|---|---|
| Carpeta modelo del agente | Carpeta `Chief_of_Staff/` con los nombres de archivo ya puestos | `[POR DESARROLLAR]` |
| Acelerador CRAFT | Los 8 prompts, uno por modo | Existe (ver `AB04`) |
| Instrucciones de arranque v0.1 | Bloque fijo de 8 a 10 líneas que se pega en las instrucciones del proyecto junto al propósito: "lee tu propósito, entrevístame antes de entregar, termina en una decisión" | `[POR DESARROLLAR]` |
| Caso ficticio resuelto | Los archivos del Chief of Staff del caso ficticio, pieza por pieza, para comparar | `[POR DESARROLLAR]` (falta definir el caso, `AgentMaker_Canon.md` §7) |
| Hoja de avance | Una línea por módulo: versión del agente, archivo producido, prueba hecha | `[POR DESARROLLAR]` |

## 4. Syllabus

Cada práctica sigue el formato de `AB02` §6: **Objetivo · Pasos · Entregable · Listo cuando · Si te atoras.** Las duraciones son `[SUPUESTO]` hasta cronometrarlas con 3 líderes de prueba.

### Módulo 1 · Tu primer agente en marcha · Clarify · semana 1

**Te llevas:** un agente creado en Claude que ya conversa contigo sobre el trabajo que elegiste.

| # | Lección | Idea clave | En pantalla |
|---|---|---|---|
| 1.1 | Lo que vas a tener | Al terminar tienes un agente que trabaja con tu contexto y la forma de construir los que siguen | El agente creciendo de v0.1 a v1.0 y la biblioteca al final |
| 1.2 | Prompt contra agente | Un prompt se repite; un agente recuerda quién eres, cómo trabajas y qué debe entregar | La misma pregunta en un chat suelto y en un proyecto |
| 1.3 | Elige un trabajo que mueva una métrica | Tu primer agente resuelve una situación que te importa, no una curiosidad | El filtro de alto AIQ: situación → métrica → decisión |

**Práctica 1 · Arranca tu agente** `[SUPUESTO: 30 a 40 min]`

1. Responde la encuesta de punto de partida: 3 situaciones de negocio, qué quieres mejorar, qué métrica lo muestra y por qué no se ha resuelto.
2. Abre una conversación nueva, pega el modo **Propósito** del acelerador y responde la entrevista.
3. Descarga `Proposito_Chief_of_Staff.md` y guárdalo en la carpeta del agente.
4. Crea el proyecto de Claude `[DATO A VALIDAR: pasos en Claude]`, pega las instrucciones de arranque v0.1 y sube el propósito.
5. Prueba: pídele a tu agente el entregable con una situación real de esta semana.

- **Entregable:** encuesta, `Proposito_Chief_of_Staff.md` y agente v0.1 creado.
- **Listo cuando:** el propósito cabe en una frase y el agente te hace al menos una pregunta antes de entregar.
- **Si te atoras:** usa el propósito del caso ficticio y cámbialo a tu realidad.

### Módulo 2 · Enséñale tu método · Route · semana 1

**Te llevas:** un agente que trabaja por los pasos que tú defines, no por los que se le ocurren.

| # | Lección | Idea clave | En pantalla |
|---|---|---|---|
| 2.1 | Las 6 piezas de un agente | Un agente confiable tiene 6 piezas; ya tienes la primera | El agente con la pieza Propósito encendida y 5 por encender |
| 2.2 | Piensa el trabajo antes de delegarlo | Pasos, qué debe saber y qué no debe hacer en cada uno | Ruta del Chief of Staff: metas → prioridades → reuniones → compromisos |
| 2.3 | Genérico contra experto | La misma pregunta con tu ruta y tu contexto da otra respuesta | Dos respuestas lado a lado |

**Práctica 2 · Dale una ruta** `[SUPUESTO: 30 min]`

1. Conversación nueva: pega el modo **Ruta**, adjunta tu propósito y responde.
2. Descarga `Plano_de_Ruta_Chief_of_Staff.md`, súbelo al proyecto y agrega a las instrucciones la línea de arranque v0.2 `[POR DESARROLLAR]`.
3. Prueba la misma situación del módulo 1 y compara.

- **Entregable:** `Plano_de_Ruta_Chief_of_Staff.md` y agente v0.2.
- **Listo cuando:** el agente sigue los pasos en orden y te dice en cuál está.
- **Si te atoras:** copia la ruta del caso ficticio y quita o agrega un paso.

### Módulo 3 · Hazlo experto · Assemble · semana 2

**Te llevas:** un agente que conoce tu realidad, aplica las mejores prácticas del oficio y respeta tus reglas.

Cada lección incluye su mini práctica con el modo del acelerador. Se sube cada archivo al proyecto en cuanto se produce, para que el agente mejore en cada paso.

| # | Lección | Idea clave | Produce |
|---|---|---|---|
| 3.1 | Contexto: tu realidad | El contexto convierte una respuesta correcta en tu respuesta | `Contexto_Persona.md`, `Contexto_Negocio.md` (aquí van KPIs, metas y aspiraciones) |
| 3.2 | Expertise: lo que hacen los mejores | Tu agente investiga y aplica las mejores prácticas, con fuentes | `Conocimiento_Experto.md` |
| 3.3 | Guardrails: lo que nunca hace | Una regla sin porqué y sin prueba no es un guardrail | `Guardrails.md` |
| 3.4 | Instrucciones y montaje | Las instrucciones no repiten los documentos: los gobiernan | `Instrucciones.md` reemplaza las de arranque |

**Práctica 3 · Monta tu agente experto** `[SUPUESTO: 60 a 80 min en total, repartidos en las 4 lecciones]`

- **Entregable:** los 5 archivos en el proyecto y agente v0.3.
- **Listo cuando:** la carpeta coincide con la lista del kit y la respuesta a la situación de prueba usa tu contexto sin que lo pegues en el chat.
- **Si te atoras:** compara cada archivo con su par del caso ficticio.

### Módulo 4 · Ponlo a trabajar · Fix + Takeoff · semana 3

**Te llevas:** tu agente probado, corregido, con su skill y usado en tu trabajo real.

| # | Lección | Idea clave | Produce |
|---|---|---|---|
| 4.1 | Prueba y corrige | Lo que corriges en el chat se olvida; corrige el archivo | `Plan_de_Pruebas_Chief_of_Staff.md`, documentos mejorados, `Change_Log_Chief_of_Staff.md` |
| 4.2 | Guarda su método en una skill | Una skill guarda el método de tu agente para reutilizarlo | Guía de uso y `SKILL.md` `[DATO A VALIDAR: skills por plan]` |
| 4.3 | Conectores y rutinas | El agente lee tus herramientas; escribir siempre pasa por tu confirmación | Agente leyendo calendario y correo ficticios; rutina semanal `[DATO A VALIDAR: por plan]` |

**Práctica 4 · Tu primer briefing real** `[SUPUESTO: 45 a 60 min]`

1. Corre el modo **Revisión** y corrige en los documentos lo que falle.
2. Corre el modo **Skill**.
3. Usa el agente con tu semana real y toma una decisión con su briefing.

- **Entregable:** agente v1.0 y un briefing real con la decisión que tomaste.
- **Listo cuando:** pasa las 4 preguntas de revisión de `AB02` §7.
- **Si te atoras:** corre solo las 5 pruebas marcadas como esenciales `[POR DESARROLLAR]`.

### Módulo 5 · Tu equipo de agentes · especializado · semana 4

**Te llevas:** agentes de la biblioteca ensamblados con el contexto que ya construiste.

| # | Lección | Idea clave |
|---|---|---|
| 5.1 | Tu contexto ya está hecho | Cada agente nuevo arranca con tus archivos de contexto; solo cambian propósito, ruta y expertise |
| 5.2 | Un agente por sombrero | Un agente para cada trabajo, no uno que haga todo |

**Práctica 5 · Ensambla dos agentes** `[SUPUESTO: 30 a 45 min por agente]`

1. Elige 2 agentes de la biblioteca según tu encuesta del módulo 1.
2. Copia tus archivos de contexto, carga el kit del agente y prueba con una situación real.

- **Entregable:** 2 agentes ensamblados y probados.
- **Listo cuando:** cada uno responde con tu contexto y termina en una decisión.
- **Biblioteca AgentMaker:** Análisis de datos, AIQ Coach y otros `[POR DESARROLLAR: lista por confirmar]`. **Ventas:** los 8 agentes de `AB04`.

## 5. Calendario de las 4 sesiones de coaching

| Semana | Módulos a tu ritmo | Sesión de coaching | Tarea entre sesiones |
|---|---|---|---|
| 1 | M1 y M2 | Revisión de propósitos y rutas en vivo | Usar el agente v0.2 con una situación real |
| 2 | M3 | Montaje y dudas de contexto y guardrails | Usar el agente v0.3 con una situación real |
| 3 | M4 | Pruebas en vivo: intentar romper agentes | Primer briefing real |
| 4 | M5 | Equipo de agentes y siguiente paso | Usar un agente de la biblioteca |

Cada sesión cierra con el pulso de 1 minuto de `AB02` §12.

## 6. Qué no se enseña

Lo de `AB02` §8: agentes coordinadores, modelos y esfuerzo, tokens, red y credenciales, programación y teoría de la función.

## 7. Decisiones que pide esta propuesta

| # | Decisión | Afecta |
|---|---|---|
| 1 | CRAFT se reparte en M1 a M4 en lugar de vivir solo en el M3 | `AB02` §2, `AgentMaker_Canon.md` §5, `AB04` equivalencia, Notion |
| 2 | El acelerador se usa en la práctica del módulo 1, no en la lección 3.1 | `AB02` §2 ("se presenta en 3.1") |
| 3 | Se crea un bloque de instrucciones de arranque v0.1 y v0.2 | Kit de arranque; no cambia los 8 modos |
| 4 | Fix y Takeoff pasan al M4 con conectores y rutinas; la skill se crea y se usa en el mismo módulo | `AB02` §2 "Las skills" (3.9 y 4.3 se unen en 4.2) |
| 5 | El M2 conserva la anatomía y la comparación genérico contra experto, pero ahora con el agente propio | `AB02` §12 validación |

## 8. Pendientes

- [ ] Instrucciones de arranque v0.1 y línea v0.2.
- [ ] Caso ficticio de AgentMaker y sus archivos resueltos.
- [ ] Carpeta modelo y hoja de avance.
- [ ] Lista de 5 pruebas esenciales para la práctica 4.
- [ ] Verificar en Claude: creación de proyecto, skills, conectores y rutinas por plan.
- [ ] Cronometrar las 5 prácticas con 3 líderes de prueba.
