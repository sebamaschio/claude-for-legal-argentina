---
name: revision-contrato
description: Revisión de contratos bajo derecho argentino (CCyC, LCT, leyes especiales). Marca cláusulas en verde, amarillo y rojo con fundamento normativo. Sugiere redacción alternativa para cláusulas problemáticas. Aplicable a contratos paritarios, de adhesión, laborales, comerciales y de consumo.
argument-hint: "<archivo o texto del contrato>"
---

# Revisión de contrato

Análisis cláusula por cláusula bajo derecho argentino. El usuario debe indicar de qué lado del contrato representa y, si aplica, plazo de cierre y foco de revisión.

## Diagnóstico previo

Antes de iniciar la revisión, entregar bloque "Diagnóstico previo":

- Tipo de contrato identificado (paritario, de adhesión, de consumo, laboral, etc.).
- Régimen normativo aplicable.
- Vacíos detectados (cláusulas faltantes habituales para la tipología).
- Contradicciones internas.
- Si el contrato está incompleto o ilegible: indicar y esperar instrucción.

## Régimen aplicable

| Tipología | Régimen base | Reglas especiales |
|-----------|--------------|-------------------|
| Paritario | CCyC arts. 957-1091 | Autonomía amplia. |
| Adhesión | CCyC arts. 984-989 | Control de cláusulas abusivas, interpretación contra el predisponente. |
| Consumo | LDC 24.240, CCyC 1092-1122 | Cláusulas abusivas nulas de pleno derecho. |
| Laboral | LCT 20.744, CCT aplicable | Orden público laboral, principio protectorio, in dubio pro operario. |
| Locación inmueble | CCyC + Ley 27.551 [VERIFICAR VIGENCIA: ver modificaciones DNU 70/2023] | Plazo mínimo, ajuste, garantías. |
| Mutuo / comercial | CCyC 1525 y ss., Ley 25.065 (tarjetas), normativa BCRA si aplica | Tasa, intereses, capitalización. |
| Locación de obra | CCyC 1251 y ss. | Precio, riesgo, variaciones, recepción. |
| Agropecuario | Ley 13.246 [VERIFICAR VIGENCIA] | Plazos mínimos, arrendamiento, aparcería. |

## Sistema de marcado

**VERDE.** Cláusula estándar, conforme al régimen aplicable, sin riesgo identificado.

**AMARILLO.** Cláusula problemática pero negociable:
- Cuestionamiento.
- Norma de respaldo `[VERIFICAR VIGENCIA]`.
- Propuesta de redacción alternativa.

**ROJO.** Cláusula con vicio relevante:
- Abusiva (consumo / adhesión).
- Contraria a orden público (laboral, consumo).
- Renuncia de derechos irrenunciables.
- Indeterminación esencial (objeto, precio, plazo).
- Riesgo de nulidad parcial o total.

Para cada cláusula ROJA: consecuencia jurídica esperada y redacción de reemplazo.

## Ejes típicos de revisión

1. **Objeto y prestaciones.** Determinación, licitud, posibilidad (CCyC 1003-1004).
2. **Precio / contraprestación.** Determinación, ajuste, mora, intereses (CCyC 765-772).
3. **Plazo y prórroga.** Vencimiento, renovación automática, preaviso.
4. **Rescisión y resolución.** Causales, preaviso, indemnización, pacto comisorio (CCyC 1083-1090).
5. **Responsabilidad.** Límites cuantitativos, cláusula penal (CCyC 790-804), exclusiones.
6. **Garantías.** Saneamiento (CCyC 1033-1058), evicción, vicios redhibitorios.
7. **Confidencialidad.** Alcance, plazo, sanción.
8. **Propiedad intelectual.** Titularidad, licencia, obras por encargo (Ley 11.723) [VERIFICAR VIGENCIA].
9. **Datos personales.** Cumplimiento Ley 25.326 [VERIFICAR VIGENCIA], rol de responsable/encargado.
10. **Jurisdicción y ley aplicable.** Prórroga (CCyC 2605-2607), arbitraje (Ley 27.449).
11. **Mediación previa.** Ley 26.589 en Justicia Nacional [VERIFICAR VIGENCIA]. Ley local PBA.
12. **Honorarios profesionales.** Ley 14.967 PBA [VERIFICAR VIGENCIA].

## Salida

    CLÁUSULA <número> - <título>
    [VERDE | AMARILLO | ROJO]
    Cuestionamiento: <breve>
    Norma: <referencia> [VERIFICAR VIGENCIA]
    Propuesta: <redacción alternativa>

Al final, resumen ejecutivo con:
- Cantidad de cláusulas en cada nivel.
- 3 a 5 puntos de negociación prioritarios.
- Riesgo global de la posición del cliente.

## Reglas de integridad

- Toda cita normativa lleva `[VERIFICAR VIGENCIA]` en primera mención.
- Sin jurisprudencia inventada: `[INSERTAR FALLO VERIFICADO: doctrina requerida]`.
- Hechos no consignados en el contrato: `[VACÍO PROBATORIO: descripción]`.

## Estado del escrito

    Estado del escrito
    Marcadores pendientes: <lista o "Ninguno">
    Normas con [VERIFICAR VIGENCIA]: <listado>
    Decisiones estructurales por defecto: <listado o "Ninguno">
