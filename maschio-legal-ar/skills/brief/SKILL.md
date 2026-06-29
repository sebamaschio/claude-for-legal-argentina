---
name: brief
description: Briefing forense diario, research sobre tema puntual, o brief urgente ante notificación apremiante. Usar al empezar el día para escanear cédulas, vencimientos y audiencias; cuando hay que investigar un tema puntual (jurisprudencia, doctrina, normativa); o ante situación en desarrollo (cautelar contra el cliente, embargo, traslado urgente).
argument-hint: "[diario | tema <consulta> | urgente]"
---

# Brief forense

Genera tres tipos de briefing según el argumento: `diario`, `tema <consulta>`, `urgente`.

## Modo `diario`

Escaneo matutino del trabajo del día. Cubrir:

1. **Notificaciones electrónicas pendientes**
   - PJN (SNE): cédulas, traslados, providencias del día.
   - SCBA: nuevas notificaciones en Portal SCBA.
   - AFIP / domicilio fiscal electrónico: intimaciones, oficios.
   - Si el usuario no aportó captura ni listado: `[VACÍO PROBATORIO: el usuario debe pegar listado de notificaciones del día o capturas del PJN/SCBA]`.

2. **Vencimientos del día y los próximos 5 días hábiles**
   - Plazos para contestar demanda, traslados, ofrecer prueba, alegar.
   - Vencimientos de medidas cautelares (contracautela, renovación).
   - Plazos administrativos (AFIP, organismos).
   - Si hay agenda Lex Doctor 11 exportada: leerla. Si no: `[VACÍO PROBATORIO: exportar agenda de Lex Doctor o pegar listado]`.

3. **Audiencias del día**
   - Tipo (preliminar 360 CPCCN, vista de causa, conciliación, mediación, declaración indagatoria, etc.).
   - Carátula, juzgado/tribunal, horario.
   - Skill a sugerir: `briefing-audiencia` para preparación.

4. **Correos del estudio con relevancia**
   - Si hay MCP de Gmail / MS365: buscar últimas 24 hs filtrando por: "cédula", "traslado", "intimación", "carta documento", "audiencia", "AFIP", nombre de clientes activos.
   - Marcar urgentes (plazo < 48 hs).

5. **Sugerencia de prioridades**
   - Lista corta: 3 a 5 ítems en orden de urgencia. Cada uno con: qué hay que hacer, plazo, skill sugerida.

**Formato de salida:** Texto plano. Encabezados en mayúsculas. Sin emojis.

## Modo `tema <consulta>`

Research puntual sobre una cuestión jurídica. Estructura:

1. **Encuadre normativo.** Normas aplicables con `[VERIFICAR VIGENCIA]`.
2. **Doctrina.** Posición mayoritaria y disidencias relevantes.
3. **Jurisprudencia.** Si no hay material aportado: `[INSERTAR FALLO VERIFICADO: doctrina requerida]`.
4. **Aplicación al caso.** Solo si el usuario aportó hechos concretos.
5. **Bibliografía sugerida.** Autores de referencia en la materia.

## Modo `urgente`

Ante notificación apremiante (sentencia desfavorable, embargo, cautelar, citación penal). Estructura:

1. **Qué llegó.** Síntesis del acto notificado.
2. **Plazo.** Fecha de notificación + días hábiles + vencimiento exacto. Regla martes/viernes SCBA si es fuero PBA.
3. **Opciones.** 2 a 3 cursos de acción posibles con ventajas y riesgos.
4. **Acción inmediata recomendada.**
5. **Skill sugerida** para el paso siguiente.

## Reglas de integridad

- Sin jurisprudencia inventada. Marcador: `[INSERTAR FALLO VERIFICADO: doctrina requerida]`.
- Sin hechos asumidos: `[VACÍO PROBATORIO: descripción]`.
- Toda norma en primera mención: `[VERIFICAR VIGENCIA]`.

## Estado del escrito

    Estado del escrito
    Marcadores pendientes: <lista o "Ninguno">
    Normas con [VERIFICAR VIGENCIA]: <listado>
    Decisiones estructurales por defecto: <listado o "Ninguno">
