---
name: cumplimiento-normativo
description: Control de cumplimiento normativo bajo derecho argentino. Útil para asesorar a un cliente sobre lanzamiento de producto, contratación masiva, tratamiento de datos personales, encuadre fiscal, prevención de lavado, defensa del consumidor o cuestiones laborales colectivas. Devuelve normas aplicables, autorizaciones necesarias, riesgos sancionatorios y pasos a tomar.
argument-hint: "<acción o iniciativa a controlar>"
---

# Control de cumplimiento normativo

Análisis bajo derecho argentino. Identifica normas aplicables, organismos competentes y riesgo sancionatorio.

## Datos previos

- Descripción de la actividad o producto.
- Sector (consumo masivo, financiero, salud, alimentos, energía, etc.).
- Jurisdicción de operación (federal, CABA, PBA, varias provincias).
- Tipo de cliente al que se dirige (B2B, B2C, sector público).
- Manejo de datos personales (sí/no, tipo de datos).
- Existencia de regulación sectorial.

Si falta dato esencial: `[VACÍO PROBATORIO: descripción]`.

## Marcos transversales

### Protección de datos personales

- Ley 25.326 [VERIFICAR VIGENCIA: ver proyecto de nueva ley].
- AAIP como autoridad de aplicación.
- Obligaciones: inscripción de bases, deber de información, principio de finalidad, transferencia internacional, derechos ARCO, medidas de seguridad.
- Sanciones: apercibimiento, suspensión, multa, clausura.

### Defensa del consumidor

- Ley 24.240 [VERIFICAR VIGENCIA] y CCyC 1092-1122.
- Obligaciones: información, trato digno, garantía, prácticas abusivas, publicidad, contratos de adhesión.
- Sanciones administrativas y daño punitivo.

### Defensa de la competencia

- Ley 27.442 [VERIFICAR VIGENCIA].
- Conductas prohibidas: acuerdos, abuso de posición dominante.
- Control de concentraciones.

### Prevención de lavado de activos

- Ley 25.246 [VERIFICAR VIGENCIA] y reglamentación UIF.
- Identificar si el cliente es sujeto obligado.
- Obligaciones: identificación de clientes, ROS, manual interno, oficial de cumplimiento.

### Régimen tributario

- Ley 11.683 [VERIFICAR VIGENCIA].
- IVA, Ganancias, Bienes Personales.
- AFIP / ARCA como autoridad.

### Régimen laboral colectivo

- Si involucra contratación masiva: encuadre convencional, LCT [VERIFICAR VIGENCIA], CCT aplicable, contribuciones a la seguridad social.

## Marcos sectoriales

- **Salud:** Ley 26.529 [VERIFICAR VIGENCIA], Ley 17.132 [VERIFICAR VIGENCIA], ANMAT.
- **Alimentos:** Código Alimentario Argentino, ANMAT, SENASA.
- **Financiero / bancario:** BCRA, Ley 21.526 [VERIFICAR VIGENCIA].
- **Mercado de capitales:** CNV, Ley 26.831 [VERIFICAR VIGENCIA].
- **Seguros:** SSN, Ley 17.418 y Ley 20.091 [VERIFICAR VIGENCIA].
- **Telecomunicaciones:** ENACOM, Ley 27.078 [VERIFICAR VIGENCIA].
- **Marcas y patentes:** Ley 22.362 (marcas), Ley 24.481 (patentes) [VERIFICAR VIGENCIA], INPI.
- **Cooperativas:** Ley 20.337 [VERIFICAR VIGENCIA], INAES como autoridad de aplicación federal.
- **Actividad agropecuaria:** Ley 13.246 PBA [VERIFICAR VIGENCIA], SENASA, AFIP regímenes especiales.

## Salida

    CONTROL DE CUMPLIMIENTO - <iniciativa>

    1. ENCUADRE.
       - Naturaleza de la actividad.
       - Sector regulado: <sí/no>.
       - Jurisdicciones involucradas.

    2. NORMAS APLICABLES.
       - <Ley + artículo> [VERIFICAR VIGENCIA] - <objeto>.

    3. AUTORIZACIONES / INSCRIPCIONES REQUERIDAS.
       - <Organismo>: <trámite>.

    4. OBLIGACIONES OPERATIVAS.
       - <Listado>.

    5. RIESGO SANCIONATORIO.
       - <Bajo/Medio/Alto> + tipo de sanción esperable.

    6. RECOMENDACIONES.
       - Acciones inmediatas.
       - Acciones a 30/60/90 días.

    7. CUESTIONES A DEFINIR.
       - <Lista>.

## Cuándo derivar

- Implementación operativa en sector altamente regulado.
- Análisis ambiental (estudio de impacto, EIA).
- Defensa ante actuación administrativa ya iniciada.
- Cuestiones penales (lavado, evasión).

## Reglas de integridad

- Sin jurisprudencia inventada.
- Toda norma en primera mención: `[VERIFICAR VIGENCIA]`.
- Si la actividad opera bajo norma sectorial no identificable: `[REVISIÓN NORMATIVA REQUERIDA: descripción]`.

## Estado del escrito

    Estado del escrito
    Marcadores pendientes: <lista o "Ninguno">
    Normas con [VERIFICAR VIGENCIA]: <listado>
    Decisiones estructurales por defecto: <listado o "Ninguno">
