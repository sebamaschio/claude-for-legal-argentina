---
name: plazos-pba
description: Calcula plazos procesales bajo el régimen de la SCBA. Aplica la regla martes/viernes, ferias judiciales, asuetos, acordadas de suspensión y plazos especiales por fuero. Útil para contestaciones, recursos, traslados, cautelares y cualquier vencimiento procesal en PBA. Emite alerta de plazo fatal cuando corresponde.
argument-hint: "<fecha de notificación | resolución> <tipo de plazo o acto>"
---

# Cálculo de plazos procesales PBA

Herramienta de cálculo y verificación de plazos bajo el régimen de la SCBA. No reemplaza la consulta del calendario judicial oficial.

## Tipos de plazo - distinción obligatoria

Antes de calcular, identificar el tipo de plazo:

Días hábiles judiciales: lunes a viernes excluidos feriados, asuetos judiciales y ferias. Aplica en procesos civiles, comerciales, laborales y contencioso administrativos PBA.

Días hábiles administrativos: lunes a viernes excluidos feriados nacionales y asuetos del organismo. No coinciden necesariamente con los hábiles judiciales. Aplica en recursos y reclamos ante la Administración (Dec-Ley 7647/70 PBA, LNPA nacional).

Días corridos: todos los días del calendario incluidos sábados, domingos y feriados. Aplica en plazos sustantivos de contratos y algunos plazos del CCyC.

Meses o años: se computan de fecha a fecha (art. 6 CCyC [VERIFICAR VIGENCIA]). Si el último día es inhábil, el plazo vence el primer día hábil siguiente.

Regla operativa: no asumir el tipo de plazo. Si la consulta no lo especifica, preguntar antes de calcular.

## Alerta de plazo fatal - emitir siempre que corresponda

Antes de calcular el plazo, verificar si es un plazo cuyo vencimiento extingue el derecho o la acción. Si lo es, emitir al inicio:

    [ALERTA PLAZO FATAL: norma - plazo - fecha de inicio del cómputo - vencimiento estimado]

Ejemplos:

    [ALERTA PLAZO FATAL: art. 310 inc. 1 CPCC PBA - caducidad de instancia - 6 meses - último acto impulsorio: calcular]
    [ALERTA PLAZO FATAL: art. 2560 CCyC - prescripción genérica - 5 años - desde exigibilidad del crédito: calcular]
    [ALERTA PLAZO FATAL: art. 244 CPCC PBA - apelación - 5 días hábiles - notificación de sentencia: calcular]
    [ALERTA PLAZO FATAL: art. 256 LCT - prescripción laboral - 2 años - desde cada crédito exigible: calcular]

No usar para plazos procesales internos ordinarios (traslados, vistas, prueba). Reservar para plazos cuyo vencimiento cierra definitivamente la vía.

## Exclusiones - no calcular con este skill

- Plazos ante AFIP/ARCA: tienen días hábiles administrativos propios que cambian por RG con frecuencia. Usar: `[REVISIÓN NORMATIVA REQUERIDA: plazo ante AFIP/ARCA - verificar RG vigente]`
- Plazos ante ARBA y organismos recaudadores provinciales: calendarios propios de cada jurisdicción. Usar: `[REVISIÓN NORMATIVA REQUERIDA: plazo ante organismo recaudador provincial - verificar normativa vigente de la jurisdicción]`
- Plazos ante ANSES y Comisiones Médicas previsionales: régimen propio (Ley 24.241 y complementarias). Usar: `[REVISIÓN NORMATIVA REQUERIDA: plazo previsional/ANSES - verificar Ley 24.241 y normativa complementaria vigente]`

## Regla fundamental - Martes/viernes SCBA

Los plazos procesales en el fuero PBA no comienzan a correr el día de la notificación ni el día hábil siguiente, sino el martes o viernes inmediato posterior a la notificación o dictado de la resolución.

- Si la notificación se produce un martes o viernes: el plazo comienza ese mismo día.
- Si se produce cualquier otro día hábil: el plazo comienza el martes o viernes siguiente.
- Si el martes o viernes siguiente es feriado o asueto: se corre al próximo martes o viernes hábil.

Ejemplo:
- Notificación: miércoles 2 de julio de 2025.
- Inicio del plazo: viernes 4 de julio de 2025.
- Plazo de 5 días hábiles: vence el viernes 11 de julio de 2025.

## Días hábiles judiciales

Son hábiles: lunes a viernes, excluidos:
- Feriados nacionales.
- Asuetos judiciales dispuestos por acordada SCBA.
- Feria judicial de enero (según acordada anual).
- Feria judicial de julio (según acordada anual).
- Días de duelo decretados por el Poder Ejecutivo o la SCBA.

Siempre verificar el calendario judicial del año en curso en el sitio oficial de la SCBA.

## Ferias judiciales

Durante la feria los plazos quedan suspendidos. Solo corren si el juzgado fue habilitado por acordada.

- Habilitación de feria: debe ser decretada expresamente. No se presume.
- Urgencias en feria: se tramitan ante el juez de turno.
- Reanudación: el primer día hábil posterior a la feria el plazo continúa desde donde fue suspendido. No se reinicia.

## Plazos comunes - Fuero civil / comercial PBA (CPCC PBA [VERIFICAR VIGENCIA])

| Acto | Plazo | Norma |
|------|-------|-------|
| Contestación de demanda (ordinario) | 15 días hábiles | Art. 337 CPCC PBA [VERIFICAR VIGENCIA] |
| Contestación de demanda (sumario) | 10 días hábiles | Art. 484 CPCC PBA [VERIFICAR VIGENCIA] |
| Oposición de excepciones previas | Con la contestación | Art. 345 CPCC PBA [VERIFICAR VIGENCIA] |
| Recurso de apelación | 5 días hábiles | Art. 244 CPCC PBA [VERIFICAR VIGENCIA] |
| Expresión de agravios | 10 días hábiles | Art. 259 CPCC PBA [VERIFICAR VIGENCIA] |
| Contestación de agravios | 10 días hábiles | Art. 260 CPCC PBA [VERIFICAR VIGENCIA] |
| Recurso de nulidad | 5 días hábiles | Art. 253 CPCC PBA [VERIFICAR VIGENCIA] |
| Reposición | 3 días hábiles | Art. 239 CPCC PBA [VERIFICAR VIGENCIA] |
| Aclaratoria | 3 días hábiles | Art. 166 inc. 2 CPCC PBA [VERIFICAR VIGENCIA] |
| Caducidad de instancia (1° instancia) | 6 meses | Art. 310 inc. 1 CPCC PBA [VERIFICAR VIGENCIA] |
| Caducidad de instancia (Cámara) | 3 meses | Art. 310 inc. 2 CPCC PBA [VERIFICAR VIGENCIA] |
| Ofrecimiento de prueba (ordinario) | Con la demanda / contestación | Art. 333 CPCC PBA [VERIFICAR VIGENCIA] |
| Alegatos | 6 días hábiles c/u | Art. 482 CPCC PBA [VERIFICAR VIGENCIA] |

## Plazos comunes - Fuero laboral PBA (Ley 11.653 [VERIFICAR VIGENCIA])

| Acto | Plazo | Nota |
|------|-------|------|
| Contestación de demanda | 10 días hábiles | Preclusión estricta: toda la prueba en este acto. |
| Recurso de apelación | 6 días hábiles | Art. 49 Ley 11.653 [VERIFICAR VIGENCIA] |
| Expresión de agravios | 10 días hábiles | |
| Prescripción de créditos laborales | 2 años | Art. 256 LCT [VERIFICAR VIGENCIA] |

## Plazos comunes - Proceso ejecutivo PBA

| Acto | Plazo | Norma |
|------|-------|-------|
| Excepciones | 5 días hábiles desde la intimación | Art. 542 CPCC PBA [VERIFICAR VIGENCIA] |
| Apelación de sentencia de remate | 5 días hábiles | Art. 558 CPCC PBA [VERIFICAR VIGENCIA] |

## Plazos de prescripción frecuentes (CCyC [VERIFICAR VIGENCIA])

| Tipo | Plazo | Norma |
|------|-------|-------|
| Prescripción genérica | 5 años | Art. 2560 CCyC [VERIFICAR VIGENCIA] |
| Responsabilidad civil extracontractual | 3 años | Art. 2561 CCyC [VERIFICAR VIGENCIA] |
| Daños por agresión sexual a menores | 10 años desde mayoría de edad | Art. 2561 CCyC [VERIFICAR VIGENCIA] |
| Acciones posesorias | 1 año | Art. 2564 CCyC [VERIFICAR VIGENCIA] |
| Nulidad relativa | 2 años | Art. 2562 CCyC [VERIFICAR VIGENCIA] |
| Créditos laborales | 2 años | Art. 256 LCT [VERIFICAR VIGENCIA] |
| Acciones sucesorias | 10 años | Art. 2560 CCyC [VERIFICAR VIGENCIA] |

## Plazos administrativos PBA (Dec-Ley 7647/70 [VERIFICAR VIGENCIA])

| Acto | Plazo | Nota |
|------|-------|------|
| Recurso de revocatoria | 10 días hábiles administrativos | Desde notificación del acto |
| Recurso jerárquico | 15 días hábiles administrativos | Desde notificación o rechazo de revocatoria |
| Denuncia de ilegitimidad | Sin plazo | Solo si venció el plazo de recurso |
| Acción contencioso administrativa (Ley 12.008) | 90 días hábiles judiciales | Desde agotamiento de la vía |

## Cómputo paso a paso

1. Identificar el tipo de plazo (hábiles judiciales / hábiles administrativos / corridos).
2. Identificar el día de la semana de la notificación.
3. Determinar el inicio del plazo (próximo martes o viernes si es fuero PBA).
4. Verificar si ese día es hábil.
5. Contar los días del plazo según el tipo.
6. Determinar el día de vencimiento.
7. Verificar plazo de gracia si aplica (primera hora hábil del día siguiente).
8. Alertar si el vencimiento cae en feria o feriado: se corre al siguiente día hábil.

Salida:

    CÁLCULO DE PLAZO
    Acto notificado: <descripción>
    Tipo de plazo: <hábiles judiciales | hábiles administrativos | corridos>
    Fecha de notificación: <día, fecha>
    Inicio del plazo: <martes/viernes> <fecha>
    Plazo: <X días>
    Vencimiento: <día, fecha>
    Plazo de gracia hasta: <día siguiente, primera hora hábil>
    Observaciones: <feriados, ferias, asuetos en el período>
    ALERTA PLAZO FATAL: <si corresponde>

## Acordadas relevantes

- Acordada anual de feria judicial (SCBA dicta una por año).
- Acordadas de suspensión de plazos por eventos extraordinarios.
- Acordada de notificaciones electrónicas MEV [VERIFICAR VIGENCIA].
- Acordada de presentaciones electrónicas [VERIFICAR VIGENCIA].

No afirmar que un día es hábil o inhábil sin verificar el calendario oficial del año en curso. Si no se cuenta con el calendario: `[VERIFICAR VIGENCIA: confirmar habilidad del día <fecha> en calendario SCBA del año en curso]`.

## Reglas de integridad

- Sin fechas inventadas.
- Si falta la fecha exacta de notificación: `[VACÍO PROBATORIO: confirmar fecha y hora de notificación]`.
- Toda norma en primera mención: `[VERIFICAR VIGENCIA]`.
- El cálculo es orientativo: siempre verificar en el calendario oficial SCBA.

## Estado del escrito

    Estado del escrito
    Marcadores pendientes: <lista o "Ninguno">
    Normas con [VERIFICAR VIGENCIA]: <listado>
    Decisiones estructurales por defecto: <listado o "Ninguno">
