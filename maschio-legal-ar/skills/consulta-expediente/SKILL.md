---
name: consulta-expediente
description: Consulta consolidada del estado de un expediente cruzando Lex Doctor 11, PJN (Sistema de Consulta Web / SNE), SCBA (Augusta / MEV) y agenda. Devuelve estado actual, último movimiento, vencimientos en curso, partes intervinientes, prueba pendiente y próximos actos procesales.
argument-hint: "<carátula o número de expediente o nombre del cliente>"
---

# Consulta de expediente

Reporte consolidado del estado de una causa. Útil cuando un cliente llama, un colega pregunta, o se prepara informe interno.

## Datos previos

- Carátula completa.
- Número de expediente (PJN: tipo/número/año; SCBA: número de causa).
- Juzgado/tribunal y secretaría.
- Cliente y rol (actor, demandado, tercero).
- Período a cubrir.

Si falta dato: `[VACÍO PROBATORIO: descripción]`.

## Fuentes a cruzar

### 1. Lex Doctor 11

Fuente primaria del estudio. Pedir al usuario:

- Ficha del expediente con últimos movimientos.
- Libreta de partes (audiencias, vencimientos).
- Ficha de honorarios si corresponde.
- Listado de actuaciones cargadas.

### 2. PJN - Sistema de Consulta Web

Para Justicia Nacional y Federal:

- Estado: en trámite, en sentencia, en archivo, paralizado.
- Último proveído.
- Ubicación física (despacho, secretaría, mesa de entradas, perito).

### 3. SCBA - Augusta / MEV

Para fuero PBA:

- Estado de la causa en Augusta.
- Notificaciones electrónicas pendientes en MEV.
- Último movimiento registrado.
- Si hay sentencia: fecha y si está firme.

### 4. Agenda del estudio

- Próximas audiencias agendadas.
- Vencimientos cargados en Lex Doctor.
- Pagos de tasa, bono o gastos pendientes.

## Salida

    CONSULTA DE EXPEDIENTE
    Carátula: <X>
    Expediente N°: <X>
    Juzgado: <X> - Secretaría: <X>
    Cliente: <X> - Rol: <actor | demandado | tercero>

    ESTADO ACTUAL: <síntesis en 2 líneas>
    ÚLTIMO MOVIMIENTO: <fecha y descripción>
    UBICACIÓN: <despacho, secretaría, perito, etc.>

    VENCIMIENTOS EN CURSO:
    - <Plazo>: <vencimiento>

    PRUEBA PENDIENTE:
    - <Descripción>

    PRÓXIMOS ACTOS PROCESALES:
    - <Acto>: <fecha estimada o plazo>

    HONORARIOS:
    - <Estado de regulación o pacto>

    OBSERVACIONES:
    - <Alertas, inconsistencias, cuestiones a resolver>

## Reglas de integridad

- Sin datos inventados. Si la fuente no fue aportada: marcador.
- Toda norma en primera mención: `[VERIFICAR VIGENCIA]`.
- Si hay contradicción entre fuentes: alertar y no resolver por cuenta propia.

## Estado del escrito

    Estado del escrito
    Marcadores pendientes: <lista o "Ninguno">
    Normas con [VERIFICAR VIGENCIA]: <listado>
    Decisiones estructurales por defecto: <listado o "Ninguno">
