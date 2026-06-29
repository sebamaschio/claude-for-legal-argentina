---
name: triage-documento
description: Triage rápido de documentos recibidos por el cliente - carta documento, demanda notificada, intimación de organismo, cédula apremiante, oficio. Clasifica como VERDE (rutinario, sin urgencia), AMARILLO (revisión y respuesta en días) o ROJO (acción inmediata, plazo perentorio o riesgo grave). Pensado para decidir en cinco minutos qué hacer con un documento que entró al estudio.
argument-hint: "<documento recibido | descripción>"
---

# Triage de documento recibido

Clasificación rápida de qué hacer con un documento que llega al estudio.

## Datos previos mínimos

- Tipo de documento (CD, demanda, intimación, cédula, oficio, acta).
- Quién lo recibió y cuándo (fecha y hora exacta de recepción).
- Remitente (parte, juzgado, organismo, abogado).
- Cliente involucrado.
- Plazo expreso o implícito de respuesta.

Si falta la fecha de recepción exacta: `[VACÍO PROBATORIO: confirmar fecha y hora de notificación]`.

## Criterios de clasificación

### ROJO - Acción en 24-72 hs

Cualquiera de:

- Cédula de notificación de demanda con plazo de contestación corriendo.
- Notificación de embargo, inhibición o cualquier cautelar contra el cliente.
- Sentencia desfavorable notificada (corre plazo de recurso).
- Citación a indagatoria, audiencia penal o detención.
- Intimación con plazo perentorio < 5 días hábiles.
- Acta de inspección o intimación AFIP/ARCA con plazo corriendo.
- Vencimiento de un plazo procesal en < 72 hs.
- Caducidad inminente (instancia, prescripción).

**Salida ROJO:**

    CLASIFICACIÓN: ROJO

    HECHO: <síntesis del documento>.
    FECHA DE RECEPCIÓN: <fecha y hora>.
    PLAZO: <vencimiento exacto con cálculo>.
    ACCIÓN INMEDIATA: <qué hacer hoy>.
    SKILL SUGERIDA: <nombre del skill para el paso siguiente>.

### AMARILLO - Acción en 3-10 días hábiles

- CD recibida con plazo de respuesta > 5 días hábiles.
- Requerimiento de organismo con plazo amplio.
- Traslado de prueba o documental sin urgencia inmediata.
- Notificación de providencia de mero trámite.
- Oficio a contestar sin plazo perentorio.

**Salida AMARILLO:**

    CLASIFICACIÓN: AMARILLO

    HECHO: <síntesis>.
    PLAZO ESTIMADO: <fecha límite>.
    ACCIÓN RECOMENDADA: <qué hacer y cuándo>.
    SKILL SUGERIDA: <nombre>.

### VERDE - Sin urgencia inmediata

- Acuse de recibo de presentación propia.
- Providencia favorable sin plazo que corra.
- Notificación de suspensión de plazos (feria, acordada).
- Documentación informativa sin requerimiento de respuesta.

**Salida VERDE:**

    CLASIFICACIÓN: VERDE

    HECHO: <síntesis>.
    ACCIÓN: Archivar / registrar en Lex Doctor.

## Cálculo de plazos - Fuero PBA

- Los plazos procesales comienzan el martes o viernes inmediato posterior al dictado o notificación de la resolución (acordadas SCBA).
- Días hábiles judiciales: lunes a viernes, excluidas ferias y asuetos.
- Feria de enero y julio: suspenden plazos salvo habilitación.
- Verificar siempre si hay acordada de suspensión vigente.

## Reglas de integridad

- Sin fecha de recepción confirmada: no calcular plazo. Marcador obligatorio.
- Toda norma en primera mención: `[VERIFICAR VIGENCIA]`.
- Si el documento no fue aportado: `[VACÍO PROBATORIO: adjuntar el documento o describir su contenido completo]`.

## Estado del escrito

    Estado del escrito
    Marcadores pendientes: <lista o "Ninguno">
    Normas con [VERIFICAR VIGENCIA]: <listado>
    Decisiones estructurales por defecto: <listado o "Ninguno">
