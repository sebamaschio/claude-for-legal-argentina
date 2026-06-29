---
name: riesgo-procesal
description: Evalúa riesgo procesal y patrimonial de un caso bajo derecho argentino. Cruza chances de éxito, exposición económica, costas, plazos críticos (caducidad, prescripción) y viabilidad de cautelar. Marca casos que requieren consulta con socio del estudio o derivación.
argument-hint: "[caso a evaluar]"
---

# Evaluación de riesgo procesal

Análisis para decidir aceptación, estrategia, transacción o derivación. Cuatro ejes: viabilidad, exposición, plazos, costo de litigar.

## Diagnóstico previo

Identificar antes de evaluar:

- Rol del cliente (actor o demandado).
- Fuero y jurisdicción.
- Pretensión (monto, especie, pedido).
- Estado actual (extrajudicial, mediación, juicio iniciado, instancia).
- Documentación aportada.

Si falta material clave: `[VACÍO PROBATORIO: descripción]`. No estimar chances sin contar al menos con el reclamo y los hechos del cliente.

## Matriz de evaluación

### Eje 1: Viabilidad jurídica

| Nivel | Criterio |
|-------|----------|
| ALTA | Norma clara aplicable, jurisprudencia mayoritaria a favor, prueba documental fuerte. |
| MEDIA | Norma con interpretación discutida, jurisprudencia dividida, prueba parcial. |
| BAJA | Encuadre jurídico forzado, jurisprudencia contraria, prueba débil o solo testimonial. |

Sin material jurisprudencial aportado: `[INSERTAR FALLO VERIFICADO: línea jurisprudencial relevante]`.

### Eje 2: Exposición económica

| Nivel | Criterio |
|-------|----------|
| ALTA | Monto supera umbral relevante para el cliente. Impacto reputacional o patrimonial significativo. |
| MEDIA | Monto significativo pero asumible. |
| BAJA | Monto menor o limitado por tope legal. |

Considerar: actualización monetaria, intereses (tasa activa BNA o pasiva promedio BCRA según jurisprudencia del fuero), costas.

### Eje 3: Plazos críticos

Identificar siempre antes de evaluar:

- **Prescripción.** Plazo aplicable (CCyC 2532 y ss. [VERIFICAR VIGENCIA], LCT 256 [VERIFICAR VIGENCIA], leyes especiales). Punto de partida. Causales de suspensión / interrupción.
- **Caducidad.** Si aplica (caducidad de instancia art. 310 CPCCN [VERIFICAR VIGENCIA] o equivalente PBA).
- **Plazo para recurrir.** Si hay sentencia o resolución notificada.
- **Plazo administrativo.** Si hay acto administrativo (Ley 19.549 [VERIFICAR VIGENCIA] o régimen local PBA).
- **Mediación previa obligatoria.** Justicia Nacional: Ley 26.589 [VERIFICAR VIGENCIA]. PBA: ley local.

Si el plazo está corriendo: marcarlo como prioridad ALTA con días restantes calculados. Aplicar regla martes/viernes SCBA si es fuero PBA.

### Eje 4: Costo y duración esperada

| Nivel | Criterio |
|-------|----------|
| ALTO | Litigio largo (>3 años en primera instancia), prueba pericial múltiple, alta probabilidad de recursos. |
| MEDIO | Litigio estándar para el fuero. |
| BAJO | Vía ejecutiva, monitoria, sumarísima, o caso transable rápido. |

Considerar: tasa de justicia (Ley 23.898 [VERIFICAR VIGENCIA] en Justicia Nacional, Ley 14.394 PBA [VERIFICAR VIGENCIA]), bono ColPro, peritos, gastos de prueba.

## Viabilidad de cautelar

Si el caso requiere o admite cautelar:

- **Verosimilitud del derecho.** Material aportado que la sustente.
- **Peligro en la demora.** Riesgo concreto.
- **Contracautela.** Tipo (juratoria, personal, real), monto estimado.
- **Norma aplicable.** CPCC PBA art. 195 y ss. [VERIFICAR VIGENCIA].
- **Tipo.** Embargo, inhibición, prohibición de contratar, anotación de litis, no innovar, innovativa, autosatisfactiva.

## Clasificación final

- **VERDE.** Aceptar / impulsar. Viabilidad alta, exposición controlada, plazos manejables.
- **AMARILLO.** Tomar con resguardos: convenio de honorarios claro, advertencia al cliente por escrito.
- **ROJO.** Reevaluar aceptación o limitar alcance del patrocinio. Casos típicos: prescripción operada, prueba imposible, exposición desproporcionada.

## Salida

    EVALUACIÓN DE RIESGO - <caso>

    1. Viabilidad jurídica: <ALTA | MEDIA | BAJA>. Fundamento: <texto>.
    2. Exposición económica: <ALTA | MEDIA | BAJA>. Monto estimado: <X>.
    3. Plazos críticos:
       - <Plazo>: <días restantes>.
    4. Costo / duración: <ALTO | MEDIO | BAJO>.
    5. Cautelar: <viable | no aplica | rechazo probable>.

    CLASIFICACIÓN: <VERDE | AMARILLO | ROJO>.

    Sugerencia: <aceptar | aceptar con resguardo | derivar | rechazar | requerir más material>.

## Reglas de integridad

- Sin jurisprudencia inventada.
- Sin hechos asumidos.
- Toda norma con `[VERIFICAR VIGENCIA]` en primera mención.

## Estado del escrito

    Estado del escrito
    Marcadores pendientes: <lista o "Ninguno">
    Normas con [VERIFICAR VIGENCIA]: <listado>
    Decisiones estructurales por defecto: <listado o "Ninguno">
