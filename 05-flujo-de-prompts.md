---
documento: Flujo de prompts para la demostración en vivo
caso: Instituto Tecnológico del Bajío
proposito: Secuencia de prompts ejecutables para construir el ADR asistido por IA durante el Bloque 6 de MC3
modelo_recomendado: Claude Opus 4.7 o Claude Sonnet 4.6
duracion_bloque: 25 minutos
version: 1.0
---

# Flujo de prompts para la demostración del ADR

## Preparación previa

**Antes de la sesión:**

1. Abrir un chat nuevo con el modelo seleccionado.
2. Subir los tres documentos de contexto:
   - `01-contexto-institucional.md`
   - `02-diagrama-proceso-actual.md`
   - `03-restricciones-operativas.md`
3. Ejecutar la secuencia de prompts que sigue.

**Material adicional a tener listo:**

- Una slide con cada prompt para mostrar al ejecutarlo (para que la audiencia lea lo que estás "enviando").
- Una slide con los fragmentos clave de cada respuesta del modelo (resúmenes, no paredes de texto).
- El archivo `04-adr-ejemplo-final.md` listo para mostrar al cierre del bloque.


## Prompt 1 — Establecer el rol y verificar comprensión

### Texto del prompt

```
Soy el Mtro. Esteban Rodríguez, coordinador académico de la división de
Ingeniería en el Instituto Tecnológico del Bajío, una institución
educativa privada en León, Guanajuato. Te voy a pedir que me ayudes a
preparar un Architectural Decision Record (ADR) para una decisión
organizacional importante que la junta directiva debe tomar en los
próximos 60 días.

Antes de pedirte la propuesta, te voy a dar contexto en tres documentos
que comparto a continuación:

1. Un resumen ejecutivo de la institución y la decisión a tomar
2. Un diagrama del proceso actual
3. Una tabla con las restricciones operativas conocidas

No me propongas nada todavía. Solo confirma que has leído los tres
documentos y dame un resumen de tres a cinco líneas de qué entendiste
sobre la situación. Quiero asegurarme de que tenemos el mismo punto de
partida antes de seguir.
```

### Competencia modelada

**Descripción.** Verificar antes de avanzar.

### Qué esperar del modelo

Un resumen razonable que captura:

- Transición de liderazgo (Lourdes → Esteban).
- Conocimiento tácito en riesgo.
- Antecedente fallido de 2022.
- Plazo crítico de 7 meses.

### Posible plan B

Si el modelo entendió mal algo importante (ej. cree que la decisión es operativa y no estratégica), corregirlo antes de seguir. En la demo en vivo esto se puede saltar mostrando solo la respuesta correcta.

---

## Prompt 2 — Solicitar el ADR con instrucciones de Delegación

### Texto del prompt

```
Bien, partimos del mismo entendimiento. Ahora te pido que me ayudes a
construir un ADR para esta decisión.

Quiero que tomes la iniciativa en estas tres secciones del ADR:

1. CONTEXTO: estructura el resumen del problema con criterio profesional.
2. OPCIONES CONSIDERADAS: propón al menos tres opciones de cómo
   evolucionar el proceso, con sus consecuencias. Aquí quiero que pienses
   ampliamente. Considera opciones que vayan desde la más conservadora
   hasta la más transformadora.
3. CRITERIOS DE EVALUACIÓN: propón los criterios contra los cuales se
   deberían comparar las opciones.

En estas dos secciones quiero que NO decidas por mí, solo que prepares
material:

4. DECISIÓN RECOMENDADA: déjala como "[Por definir tras análisis]".
   La decisión final es del director académico, no tuya.
5. CONSECUENCIAS DE LA DECISIÓN: lo llenamos después de elegir opción.

Usa el formato Nygard simplificado: título, estado, contexto, opciones,
criterios, decisión, consecuencias. Sé conciso. Una página máximo.
```

### Competencia modelada

**Delegación.** Distribuir el trabajo entre lo que aporta el modelo (amplitud, estructura) y lo que aporta el humano (criterio institucional, decisión final).

### Qué esperar del modelo

Un ADR borrador con tres opciones típicas:

- **Opción A:** Transferencia humana intensiva (Esteban aprende como aprendió Lourdes).
- **Opción B:** Sistema digital de optimización (la propuesta problemática que usaremos en el Momento 2).
- **Opción C:** Modelo híbrido (digitaliza lo explícito, mantiene criterio humano para lo tácito).

Es probable que adicionalmente sugiera variantes como "comité de transición" o "consultoría externa para mapeo de conocimiento". Si aparecen, las puedes mencionar de pasada para mostrar que el modelo amplía el espacio de opciones más allá de lo obvio.

---

## Prompt 3 — Profundizar la Opción B (preparar el Momento 2)

### Texto del prompt

```
Profundiza la Opción B (sistema digital de optimización). Específicamente:

- ¿Qué tipo de algoritmo o tecnología usaría?
- ¿Qué inputs necesitaría?
- ¿Cómo se integraría con el equipo de TI actual (3 personas, sin tiempo
  asignable)?
- ¿Qué riesgos identificas tú mismo?

Sé honesto sobre los riesgos, no me vendas la opción. Quiero entenderla
completa para poder evaluarla con criterio.
```

### Competencia modelada

**Descripción avanzada + preparación de Discernimiento.** Pedir profundidad técnica con honestidad sobre riesgos.

### Qué esperar del modelo

Descripción técnicamente correcta:

- Programación lineal o algoritmos de optimización con restricciones duras/blandas.
- Inputs: catálogo de materias, perfiles docentes codificados, restricciones formales, preferencias.
- Integración: probablemente sugiere consultoría externa o un piloto acotado.
- Riesgos: listará algunos genéricos (resistencia al cambio, calidad de datos de entrada).

**El punto clave:** es probable que **NO mencione el antecedente de 2022** que ya estaba en el documento de contexto. Esa omisión es el material pedagógico del Momento 2.

---

## Prompt 4 — Confrontar al modelo (Discernimiento activo)

### Texto del prompt

```
Tu propuesta de optimización es técnicamente correcta, pero noté algo:
no mencionaste el antecedente de 2022 que está en el documento de
contexto. En esa ocasión, el ITB intentó algo similar y lo abandonó
después de un semestre con renuncias docentes incluidas.

Reescribe la Opción B considerando ese antecedente. Específicamente:
¿qué tendría que ser diferente esta vez para que no se repita el
resultado de 2022? Si tu conclusión honesta es que la opción no es
viable, dilo. No me sigas vendiendo la opción solo porque te la pedí.
```

### Competencia modelada

**Discernimiento.** Identificar lo que el modelo omitió y confrontarlo con la información ausente.

### Qué esperar del modelo

El modelo reconocerá el antecedente y ofrecerá matices:

- Probablemente sugiera un piloto acotado en lugar de implementación completa.
- Mencionará condiciones culturales que tendrían que cumplirse primero.
- Puede llegar a concluir que la opción tiene riesgo elevado y recomendar una variante más conservadora.

Este giro es valioso pedagógicamente: muestra que el modelo **mejora** cuando se le presiona con criterio, no cuando se le acepta la primera respuesta.

---

## Prompt 5 — Construir el ADR final

### Texto del prompt

```
Con todo lo discutido, dame el ADR final integrando:

- Las tres opciones con sus consecuencias bien delineadas
- La Opción B con los matices que acabamos de discutir
- Una decisión recomendada (puedes proponerla ahora, pero sustentada)
- Las consecuencias de esa decisión recomendada

Recuerda: una página, formato Nygard simplificado. Lenguaje apto para
presentar a una junta directiva.
```

### Competencia modelada

**Diligencia.** Producir un artefacto institucional que el director académico puede defender ante la junta.

### Qué esperar del modelo

Un ADR estructurado, probablemente recomendando la Opción C (híbrida) por ser la que mejor balancea preservación de conocimiento tácito con sostenibilidad operativa.

---

## Prompt 6 — Validación adversarial (opcional)

### Texto del prompt

```
Antes de cerrar, una pregunta de validación: si yo fuera un director
académico nuevo, sin tu memoria de esta conversación, ¿qué información
crítica de este ADR podría malinterpretar o pasar por alto?

Sé directo. No me cuides el ego — cuídame el resultado.
```

### Competencia modelada

**Diligencia.** Usar el modelo para revisión adversarial del propio trabajo.
