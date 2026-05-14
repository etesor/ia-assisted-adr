---
documento: Diagrama del proceso actual
caso: Instituto Tecnológico del Bajío
proposito: Material de soporte para demostración de ADR asistido por IA
version: 1.0
---

# Diagrama del proceso actual de asignación de carga académica

## Visualización del flujo

```mermaid
flowchart TD
    A[Inicio del semestre<br/>noviembre o abril] --> B[Inputs disponibles]

    B --> B1[Materias del plan<br/>de estudios a cubrir<br/>~340 grupos]
    B --> B2[Docentes disponibles<br/>~180 personas]
    B --> B3[Restricciones formales<br/>titulación, experiencia,<br/>perfil PRODEP]
    B --> B4[Solicitudes especiales<br/>carga reducida, sabáticos,<br/>intercambios]
    B --> B5[Retroalimentación<br/>del semestre anterior<br/>evaluaciones de alumnos]

    B1 & B2 & B3 & B4 & B5 --> C{Proceso de decisión<br/>de la Mtra. Lourdes<br/>~3 semanas}

    C -.->|Criterios académicos| D1[Perfil docente<br/>vs. materia]
    C -.->|Criterios relacionales| D2[Conflictos históricos<br/>entre docentes y coordinadores]
    C -.->|Criterios estratégicos| D3[Materias críticas<br/>para indicadores institucionales]
    C -.->|Criterios personales| D4[Situación familiar,<br/>salud, etapa de carrera]

    D1 & D2 & D3 & D4 --> E[Matriz semestral<br/>180 docentes × 340 grupos]

    E --> F[Comunicación individual<br/>con cada docente<br/>~2 semanas]

    F --> G{Ajustes finales<br/>por excepciones}

    G -->|Renuncias de último momento| H1[Reasignación urgente]
    G -->|Materias nuevas| H2[Búsqueda de docente]
    G -->|Conflictos no anticipados| H3[Negociación 1-a-1]

    H1 & H2 & H3 --> I[Carga semestral<br/>publicada e implementada]

    style C fill:#f9d71c,stroke:#333,stroke-width:3px
    style D1 fill:#e8e8e8
    style D2 fill:#e8e8e8
    style D3 fill:#e8e8e8
    style D4 fill:#e8e8e8
```

## Descripción del flujo

### Inputs (cada noviembre y abril)

El proceso inicia con la consolidación de cinco fuentes de información:

1. **Materias a cubrir** — aproximadamente 340 grupos según el plan de estudios vigente, distribuidos entre los tres campus y los dos turnos.
2. **Docentes disponibles** — los 180 docentes con su carga histórica, disponibilidad declarada y estatus contractual.
3. **Restricciones formales** — perfil de titulación requerido para cada materia, experiencia mínima, requisitos PRODEP/SEP cuando aplican.
4. **Solicitudes especiales** — peticiones de carga reducida (por estudios, salud, investigación), sabáticos programados, solicitudes de intercambio de turno.
5. **Retroalimentación del semestre anterior** — evaluaciones de alumnos, reportes de coordinadores, incidentes documentados.

### Proceso de decisión (caja negra de ~3 semanas)

La Mtra. Lourdes opera el cruce de información durante aproximadamente tres semanas. Su proceso de pensamiento no está formalmente documentado, pero cruza al menos cuatro tipos de criterios:

- **Criterios académicos.** Perfil docente versus exigencia de la materia.
- **Criterios relacionales.** Conflictos históricos entre docentes y coordinadores, dinámicas de academia, antipatías documentadas o conocidas.
- **Criterios estratégicos.** Materias críticas para indicadores institucionales (ej. índices de reprobación monitoreados por dirección general).
- **Criterios personales.** Situación familiar, salud, etapa de carrera profesional del docente.

Los criterios académicos y formales pueden codificarse. Los relacionales y personales operan en un espacio que la Mtra. Lourdes maneja desde su memoria y su relación de 16 años con el cuerpo docente.

### Output inicial

Matriz semestral de aproximadamente 180 docentes contra 340 grupos. Cada celda asigna o no a un docente a un grupo específico, con turno y campus definidos.

### Comunicación individual (~2 semanas)

Lourdes comunica personalmente la asignación a cada docente. Esta etapa no es ceremonial: es donde surgen ajustes finos, renegociaciones y descubrimientos de incompatibilidades no anticipadas.

### Ajustes finales por excepciones

Tres tipos comunes de excepciones que requieren intervención adicional:

- **Renuncias de último momento** — docentes que dejan la institución después de publicada la asignación inicial.
- **Materias nuevas** — adecuaciones de plan de estudios o materias optativas con demanda no anticipada.
- **Conflictos no anticipados** — choques de horario, restricciones personales no comunicadas previamente, cambios en coordinaciones.

### Implementación final

Carga semestral publicada oficialmente e implementada al inicio del semestre lectivo.
