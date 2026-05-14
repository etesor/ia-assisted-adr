---
documento: ADR final como artefacto de cierre
caso: Instituto Tecnológico del Bajío
proposito: Ejemplo del producto terminado que se muestra al cierre del Bloque 6 de MC3
formato: Nygard simplificado
version: 1.0
nota: Este es un artefacto de demostración construido para fines pedagógicos. Refleja el tipo de resultado que el proceso de ADR asistido por IA puede producir cuando se aplican las cuatro competencias del framework AI Fluency.
---

# ADR-001: Evolución del proceso de asignación de carga académica

**Estado:** Propuesto · Pendiente de aprobación por Junta Directiva

**Fecha:** [Fecha de la propuesta]

**Dueño:** Director Académico designado

**Personas consultadas:** Mtra. Lourdes Aguilar (Directora Académica actual), Mtro. Esteban Rodríguez (sucesor designado), Coordinación de TI, Junta Directiva (revisión final)

---

## Contexto

La Mtra. Lourdes Aguilar, Directora Académica del ITB durante 16 años, dejará su rol en 7 meses. Una de sus responsabilidades centrales — la asignación semestral de carga académica para 180 docentes en 340 grupos — depende significativamente de conocimiento tácito acumulado sobre el cuerpo docente: relaciones, conflictos históricos, situaciones personales, dinámicas de academia.

Su sucesor designado, el Mtro. Esteban Rodríguez, es académicamente competente pero no posee ese conocimiento. La institución debe decidir cómo evolucionará el proceso para preservar la ventaja competitiva del clima docente (rotación 4% vs. 15-18% del sector) sin comprometer la sostenibilidad operativa post-transición.

Existe un antecedente relevante de 2022, cuando un intento de digitalización del proceso fue abandonado tras resistencia y renuncias docentes.

## Opciones consideradas

### Opción A — Transferencia humana intensiva

Período de cinco meses donde Lourdes y Esteban trabajan en paralelo, documentando criterios y construyendo relaciones uno-a-uno con docentes clave.

**Pros:** Preserva el modelo actual, respeta cultura institucional, no introduce tecnología nueva.

**Contras:** Dependencia de transferencia perfecta en tiempo limitado. El conocimiento tácito por definición no se transfiere completamente en cinco meses cuando se construyó en 16 años. Si Esteban dejara el rol más adelante, el problema vuelve a empezar de cero.

### Opción B — Sistema digital de optimización

Implementación de software de asignación que codifica restricciones formales y aplica algoritmos de optimización para generar la matriz semestral.

**Pros:** Eficiencia, escalabilidad, robustez ante rotación del director académico.

**Contras:** Precedente fallido de 2022 con renuncias docentes documentadas. Restricciones tácitas críticas (información de salud, acuerdos informales de retención) no codificables o codificables a costa de violar privacidad. Aversión cultural documentada en la junta directiva al "trato de docentes como recursos intercambiables." Capacidad técnica interna limitada para sostener un sistema así.

**No recomendada en su forma pura.**

### Opción C — Modelo híbrido con codificación selectiva

Mantener la decisión humana como mecanismo central, asistida por una herramienta digital que codifica solo las restricciones formales y documentables (perfiles, restricciones administrativas, conflictos de horario, datos de PRODEP). El criterio relacional y contextual permanece en el dueño del proceso. Esteban toma el rol con apoyo de un tablero estructurado que sistematiza lo sistematizable.

**Pros:** Preserva la naturaleza humana del proceso. Aprovecha tecnología donde aporta valor sin invadir donde no debe. Permite al sucesor enfocarse en construir relaciones (lo intransferible) en lugar de operar restricciones formales (lo codificable). Robustez incremental.

**Contras:** Requiere diseño cuidadoso para definir qué se codifica y qué no. Más complejo de implementar que A o B en su forma pura. Riesgo de que el tablero se convierta en muleta y desincentive la construcción de relaciones.

## Criterios de evaluación

Las opciones se evaluaron contra cuatro criterios institucionales:

1. **Preservación de la ventaja competitiva institucional** — mantener el clima docente como diferenciador.
2. **Sostenibilidad operativa** — sin requerir nuevos puestos administrativos.
3. **Compatibilidad con cultura institucional declarada** — respetar la postura de la junta directiva sobre el trato docente.
4. **Robustez ante rotación futura del dueño del proceso** — no recrear la misma dependencia personal en cinco años.

## Decisión recomendada

**Opción C — Modelo híbrido con codificación selectiva.**

Esta opción es la única que satisface simultáneamente los cuatro criterios. La Opción A es sostenible solo mientras Esteban permanezca; la Opción B tiene precedente fallido y choca con cultura institucional. La Opción C permite avanzar sin repetir el error de 2022.

## Consecuencias

### Lo que se requiere para implementar

- Se requieren tres meses para diseñar el tablero estructurado, en paralelo con la transferencia humana entre Lourdes y Esteban.
- El tablero codifica únicamente: perfiles docentes, restricciones formales SEP/PRODEP, conflictos de horario, capacidad por campus, historial de evaluaciones cuantitativas.
- El tablero **no codifica:** información de salud, acuerdos informales de retención, dinámicas de academia, situaciones familiares no declaradas formalmente.
- Esteban asume el rol con la herramienta como apoyo, no como operador de un sistema automatizado.

### Lo que se asume

- El conocimiento tácito sigue dependiendo de la persona del director académico — esto se asume como característica del modelo institucional, no como defecto a eliminar.
- La institución documenta este ADR como precedente para futuras transiciones de roles con conocimiento tácito alto.

### Riesgos gestionados

- **Si Esteban no logra construir relaciones equivalentes en dos años**, será momento de reevaluar — posiblemente con un esquema de mentoría externa o redistribución del rol.
- **Si el tablero se vuelve muleta** y Esteban descuida las relaciones, el indicador de rotación docente lo evidenciará antes de que se convierta en crisis. Se establece revisión semestral del indicador en la junta directiva.
- **Si en algún momento se requiere escalar el modelo** (apertura de un cuarto campus, por ejemplo), este ADR se reabre para evaluación.

### Lo que NO se decide en este ADR

- El diseño técnico específico del tablero (eso es decisión operativa posterior).
- La selección de proveedor o herramienta (si aplica).
- La política institucional sobre documentación de información personal de docentes (esa es decisión más amplia que excede este proceso).

---

## Nota metodológica

Este ADR fue construido con asistencia de un modelo de IA, aplicando el framework AI Fluency de Anthropic:

- **Descripción.** El director académico proporcionó al modelo el contexto institucional completo, el diagrama del proceso actual y la tabla de restricciones operativas.
- **Delegación.** El director delegó al modelo la generación de opciones, consecuencias y criterios de evaluación. Retuvo la autoridad sobre la decisión recomendada.
- **Discernimiento.** El director identificó que la Opción B propuesta inicialmente por el modelo era técnicamente correcta pero ignoraba el antecedente de 2022. Confrontó al modelo con esa información para obtener una versión más realista de la opción.
- **Diligencia.** El director es dueño del resultado. Si la junta cuestiona cualquier elemento del ADR, el director debe responder con criterio propio, no con "el modelo lo propuso así." La IA aceleró el camino; la responsabilidad institucional permanece humana.