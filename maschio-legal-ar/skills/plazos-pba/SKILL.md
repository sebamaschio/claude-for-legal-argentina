---
name: plazos-pba
description: Calcula plazos procesales bajo el régimen de la SCBA. Aplica la regla martes/viernes, ferias judiciales, asuetos, acordadas de suspensión y plazos especiales por fuero. Útil para contestaciones, recursos, traslados, cautelares y cualquier vencimiento procesal en PBA.
argument-hint: "<fecha de notificación | resolución> <tipo de plazo o acto>"
---

# Cálculo de plazos procesales PBA

Herramienta de cálculo y verificación de plazos bajo el régimen de la SCBA. No reemplaza la consulta del calendario judicial oficial.

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
| Acciones posesorias | 1 año | Art. 2564 CCyC [VERIFICAR VIGENCIA] |
| Nulidad relativa | 2 años | Art. 2562 CCyC [VERIFICAR VIGENCIA] |
| Créditos laborales | 2 años | Art. 256 LCT [VERIFICAR VIGENCIA] |
| Acciones sucesorias | 10 años | Art. 2560 CCyC [VERIFICAR VIGENCIA] |

## Cómputo paso a paso

Cuando el usuario aporte una fecha de notificación, calcular así:

1. Identificar el día de la semana de la notificación.
2. Determinar el inicio del plazo (próximo martes o viernes).
3. Verificar si ese día es hábil (no feriado, no asueto, no feria).
4. Contar los días hábiles del plazo (excluir sábados, domingos, feriados, asuetos).
5. Determinar el día de vencimiento.
6. Verificar plazo de gracia si aplica (primera hora hábil del día siguiente).
7. Alertar si el vencimiento cae en feria o feriado: se corre al siguiente día hábil.

Salida:

    CÁLCULO DE PLAZO
    Acto notificado: <descripción>
    Fecha de notificación: <día, fecha>
    Inicio del plazo: <martes/viernes> <fecha>
    Plazo: <X días hábiles>
    Vencimiento: <día, fecha>
    Plazo de gracia hasta: <día siguiente, primera hora hábil>
    Observaciones: <feriados, ferias, asuetos en el período>
    ALERTA: <si hay riesgo de error en el cálculo>

## Acordadas relevantes

Mencionar siempre que apliquen:
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
