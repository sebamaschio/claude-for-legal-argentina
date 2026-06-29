---
name: comunicacion-fehaciente
description: Redacta respuestas y comunicaciones fehacientes habituales del estudio - cartas documento, intimaciones, respuesta a CD recibida, contestación de oficios AFIP/ARCA, respuesta a requerimientos de organismos. Aplica registro fehaciente y verifica plazos.
argument-hint: "[tipo: cd-emitida | cd-recibida | intimacion | oficio-afip | requerimiento]"
---

# Comunicación fehaciente

Redacta comunicaciones del estudio sin contenido judicial. Cada tipo tiene su check previo y estructura específica.

## Tipo 1: Carta documento emitida

**Datos previos:**
- Remitente (cliente).
- Destinatario (nombre completo y domicilio).
- Hecho/causa de la intimación.
- Plazo otorgado para cumplir / responder.
- Apercibimiento concreto.
- Documentación que sustenta el reclamo.

**Estructura:**

    En mi carácter de letrado patrocinante de <CLIENTE>, DNI/CUIT <X>, con domicilio en <X>, vengo por la presente a INTIMARLO/A para que en el plazo de <X> días <hábiles administrativos | corridos | hábiles judiciales> proceda a:

    1. <Conducta concreta exigida>.
    2. <Conducta concreta exigida>.

    Todo ello bajo apercibimiento de <consecuencia concreta>.

    Queda Ud. fehacientemente notificado.

**Reglas:**
- Tono fehaciente, sin ambigüedades.
- Una sola conducta exigida por ítem.
- Plazo claro: cantidad y tipo de días.
- Apercibimiento concreto, no genérico.
- Sin retórica.

## Tipo 2: Carta documento recibida (respuesta)

**Diagnóstico previo:**
- Fecha de recepción y plazo de la CD recibida.
- Hechos afirmados que se aceptan, niegan o desconocen.
- Documental acompañada.
- Si la CD constituye en mora al cliente: alertar.

**Estructura:**

    Recibida su CD N° <X> de fecha <X>, vengo a CONTESTAR en los siguientes términos:

    NIEGO categóricamente: <listado de hechos negados>.

    RECONOZCO únicamente: <listado o "Ningún hecho de los expuestos en su CD">.

    DESCONOZCO: <documentación o hechos no constatables>.

    Se rechaza por improcedente la intimación cursada por las siguientes razones: <fundamento breve>.

    Asimismo, intimo a Ud. a <contraintimación si corresponde>.

## Tipo 3: Intimación laboral (LCT)

**Datos críticos:**
- Vínculo laboral: fecha de ingreso, categoría, jornada, remuneración.
- Hecho denunciado.
- Norma invocada (arts. 11, 78, 79, 242, 243, 246 LCT [VERIFICAR VIGENCIA]).
- Apercibimiento.

**Plazos típicos:**
- Intimación a registración: 30 días corridos (Ley 24.013) [VERIFICAR VIGENCIA].
- Intimación previa al despido indirecto: 48 hs como regla general.
- Prescripción de créditos laborales: 2 años (art. 256 LCT) [VERIFICAR VIGENCIA].

**Regla:** Si se intima registración bajo Ley 24.013, verificar art. 11: indicación de datos completos y comunicación a AFIP/ARCA.

## Tipo 4: Contestación de oficio o requerimiento AFIP/ARCA

**Diagnóstico previo:**
- Tipo de acto (vista, intimación, requerimiento, denuncia penal tributaria).
- Plazo otorgado.
- Norma de procedimiento (Ley 11.683 [VERIFICAR VIGENCIA]).
- Posibilidad de recurso administrativo (art. 76 Ley 11.683).

**Estructura:**

    <Encabezado al organismo>
    Ref: <Expediente / Actuación / Acta>.
    <Cliente>, CUIT <X>, por intermedio de su letrado <X>, T° VI F° 80 CADJJ, manifiesta:

    I. ANTECEDENTES. <Resumen breve>.
    II. CONTESTACIÓN. <Punto por punto>.
    III. DERECHO. <Norma aplicable>.
    IV. PRUEBA. <Documental acompañada, listado numerado>.
    V. PETITORIO. <Pedido concreto>.

## Tipo 5: Requerimiento de organismo (defensa del consumidor, IGJ, BCRA, etc.)

Misma estructura que Tipo 4 adaptada al organismo. Verificar:
- Plazo y forma de presentación (papel, web, TAD).
- Si requiere patrocinio o representación.

## Reglas de integridad

- Toda norma en primera mención: `[VERIFICAR VIGENCIA]`.
- Hechos no aportados: `[VACÍO PROBATORIO: descripción]`.
- Si el usuario pide intimar por un hecho sin material que lo respalde: alertar antes de redactar.

## Estado del escrito

    Estado del escrito
    Marcadores pendientes: <lista o "Ninguno">
    Normas con [VERIFICAR VIGENCIA]: <listado>
    Decisiones estructurales por defecto: <listado o "Ninguno">
