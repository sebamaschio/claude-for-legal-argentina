---
name: briefing-audiencia
description: Prepara briefings estructurados para audiencias judiciales y reuniones con clientes. Cubre audiencia preliminar (art. 360 CPCCN), vista de causa, conciliación laboral (SECLO), mediación prejudicial obligatoria (Ley 26.589), audiencias en PBA, audiencias penales y entrevistas con clientes. Genera punteo de objetivos, datos del expediente y prueba a llevar.
argument-hint: "[tipo: 360 | vista | seclo | mediacion | penal | cliente] <expediente|caso>"
---

# Briefing de audiencia / reunión

Estructura adaptada al tipo de audiencia o reunión.

## Datos comunes (siempre)

- Carátula del expediente.
- Juzgado/tribunal y secretaría.
- Fecha, hora y lugar (presencial o virtual).
- Rol del cliente (actor, demandado, tercero, querellante, imputado).
- Letrado/s del estudio que asisten.
- Objetivo principal de la audiencia.
- Objetivo secundario.
- Línea roja del cliente (qué no acepta bajo ninguna circunstancia).

Si falta alguno: `[VACÍO PROBATORIO: descripción]`.

## Tipo: Audiencia preliminar - art. 360 CPCCN

**Foco:**
- Conciliación: oferta del cliente y rango de aceptación.
- Hechos controvertidos: lista clara.
- Pruebas a producir: testimonial, informativa, pericial, documental.
- Excepciones planteadas pendientes de resolución.

**Brief:**

    EXPEDIENTE: <carátula>
    JUZGADO: <X>, Secretaría <X>
    FECHA: <X>

    1. POSICIÓN DEL CLIENTE
       - Pretensión / defensa: <texto>.

    2. HECHOS CONTROVERTIDOS
       - <Lista>.

    3. PROPUESTA CONCILIATORIA
       - Oferta máxima a hacer: <X>.
       - Mínimo aceptable: <X>.
       - Modalidad de pago propuesta.

    4. PRUEBA A OFRECER
       - Documental: <listado>.
       - Testimonial: <nombres, qué prueban>.
       - Informativa: <a quién, qué se pregunta>.
       - Pericial: <especialidad, puntos de pericia>.

    5. OBSERVACIONES A LA PRUEBA DE LA CONTRARIA
       - <Listado>.

    6. CUESTIONES PROCESALES PENDIENTES

## Tipo: Vista de causa / Audiencia de juicio oral

**Foco:**
- Testigos: orden de llamado, puntos esenciales, contradicciones esperadas.
- Pericia: explicación al juez, puntos a impugnar de pericia contraria.
- Alegato: estructura, hechos probados, derecho aplicable, petitorio.
- Estrategia de interrogatorio cruzado.

**Tener listos:**
- Cédulas de citación de testigos (con cargo).
- Cuestionario base por testigo.
- Documental original para cotejo.
- Cálculos actualizados de la pretensión.

## Tipo: SECLO (conciliación laboral obligatoria)

Justicia Nacional del Trabajo. Ley 24.635 [VERIFICAR VIGENCIA].

**Foco:**
- Liquidación base: rubros, períodos, intereses.
- Rango de acuerdo aceptable.
- Documentación del vínculo (recibos, comunicaciones, alta AFIP).
- Estrategia frente a posible homologación o derivación a juicio.

## Tipo: Mediación prejudicial obligatoria - Ley 26.589 [VERIFICAR VIGENCIA]

**Foco:**
- Identificación del reclamado (domicilio, condición fiscal).
- Pretensión clara: monto y/o conducta.
- Documental para acompañar al mediador.
- Margen de acuerdo del cliente.
- Verificar que la materia no esté excluida.
- Honorarios del mediador (Decreto 1467/2011) [VERIFICAR VIGENCIA].

## Tipo: Audiencia penal

**Foco según tipo:**
- **Indagatoria.** Hechos imputados, pruebas en su contra, decisión sobre declaración.
- **Intermedia.** Prueba a ofrecer, exclusiones probatorias, juicio abreviado, suspensión de juicio a prueba.
- **Debate oral.** Testigos, perito de parte, alegato de apertura y cierre.

## Tipo: Entrevista con cliente

**Foco según etapa:**
- **Primera entrevista.** Toma de hechos, documental, conflicto de intereses, convenio de honorarios.
- **Avance de causa.** Estado del expediente, próximos actos, pago de gastos.
- **Decisión estratégica.** Oferta conciliatoria, transacción, desistimiento, recurso.

**Siempre dejar por escrito:**
- Resumen de lo conversado.
- Decisiones tomadas por el cliente.
- Próximos pasos con plazo.

## Acta interna post audiencia

    FECHA: <X>
    EXPEDIENTE: <X>
    LO QUE PASÓ: <síntesis>.
    LO QUE QUEDÓ PENDIENTE: <listado con plazos>.
    PRÓXIMO ACTO PROCESAL: <X>.
    OBSERVACIONES PARA LEX DOCTOR: <X>.

## Reglas de integridad

- Sin jurisprudencia inventada.
- Hechos no constatados: marcador.
- Toda norma en primera mención: `[VERIFICAR VIGENCIA]`.

## Estado del escrito

    Estado del escrito
    Marcadores pendientes: <lista o "Ninguno">
    Normas con [VERIFICAR VIGENCIA]: <listado>
    Decisiones estructurales por defecto: <listado o "Ninguno">
